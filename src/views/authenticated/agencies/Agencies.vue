<script setup>
import { ref, defineProps } from "vue";
const props = defineProps(["locations", "success", "agencies"]);
const agency = ref({
    name: null,
    phone: null,
    address: null,
    email: null,
    password: null,
    location: null,
    logo: null,
});
const addModal = ref(false);
const editModal = ref(false);

const expandedRows = [];
</script>

<template>
    <Authenticated>
        <Toast />
        <div class="flex justify-between">
            <h2 class="text-2xl font-semibold capitalize">liste des agences</h2>
            <Button
                class="p-button-sm p-button-info"
                icon="pi pi-plus"
                label="Nouveau"
                @click="addModal = true"
            />
        </div>

        <!--add agency modal-->
        <Dialog
            v-model:visible="addModal"
            :modal="true"
            class="w-full md:w-1/2"
        >
            <template #header>
                <h3 class="font-semibold">Ajouter un agence</h3>
            </template>
            <form class="mt-2">
                <ValidationErrors />
                <div class="mt-6">
                    <span class="p-float-label">
                        <InputText
                            v-model.trim="agency.name"
                            class="w-full"
                            type="text"
                        />
                        <label>Nom d'agence</label>
                    </span>
                </div>
                <div class="mt-6">
                    <span class="p-float-label">
                        <InputText
                            id="phone"
                            v-model.trim="agency.phone"
                            class="w-full"
                            type="tel"
                        />
                        <label for="phone">Téléphone</label>
                    </span>
                </div>
                <div class="mt-6">
                    <span class="p-float-label">
                        <InputText
                            id="address"
                            v-model.trim="agency.address"
                            class="w-full"
                            type="text"
                        />
                        <label for="address">Adresse</label>
                    </span>
                </div>
                <div class="mt-6">
                    <Dropdown
                        v-model="agency.location"
                        :filter="true"
                        :options="locations"
                        class="w-full"
                        optionLabel="name"
                        optionValue="id"
                        placeholder="Sélectionnez une ville"
                    />
                </div>
                <div class="mt-6">
                    <span class="p-float-label">
                        <InputText
                            id="email"
                            v-model="agency.email"
                            class="w-full"
                            type="email"
                        />
                        <label>Adresse email</label>
                    </span>
                </div>
                <div class="mt-6">
                    <span class="p-float-label">
                        <Password
                            v-model="agency.password"
                            :feedback="false"
                            class="w-full"
                            inputClass="w-full"
                            toggleMask
                        />
                        <label>Mot de passe</label>
                    </span>
                </div>
                <div class="mt-6">
                    <input accept="image/*" class="w-full" type="file" />
                    <progress v-if="progress" :value="percentage" max="100">
                        {{ percentage }}%
                    </progress>
                </div>
                <div class="mt-6">
                    <Button
                        :loading="processing"
                        class="w-full p-button-info"
                        icon="pi pi-check"
                        label="Ajouter"
                        type="submit"
                    />
                </div>
            </form>
        </Dialog>

        <!--edit agency modal-->
        <!-- <Dialog
            v-model:visible="editDisplay"
            :modal="true"
            class="w-full md:max-w-2xl"
        >
            <template #header>
                <h3 class="font-semibold">Modifier un agence</h3>
            </template>
            <form class="mt-2" @submit.prevent="update">
                <ValidationErrors />
                <div class="mt-6">
                    <span class="p-float-label">
                        <InputText
                            id="name"
                            v-model.trim="agency.name"
                            class="w-full"
                            type="text"
                        />
                        <label for="name">Nom complete</label>
                    </span>
                </div>
                <div class="mt-6">
                    <span class="p-float-label">
                        <InputText
                            v-model.trim="agency.agencyName"
                            class="w-full"
                            type="text"
                        />
                        <label>Nom d'agence</label>
                    </span>
                </div>
                <div class="mt-6">
                    <span class="p-float-label">
                        <InputText
                            v-model.trim="agency.phone"
                            class="w-full"
                            type="tel"
                        />
                        <label for="phone">Téléphone</label>
                    </span>
                </div>
                <div class="mt-6">
                    <span class="p-float-label">
                        <InputText
                            v-model.trim="agency.address"
                            class="w-full"
                            type="text"
                        />
                        <label for="address">Adresse</label>
                    </span>
                </div>
                <div class="mt-6">
                    <Dropdown
                        v-model="agency.selectedLocation"
                        :filter="true"
                        :options="locations"
                        class="w-full"
                        optionLabel="name"
                        optionValue="id"
                        placeholder="Sélectionnez une ville"
                    />
                </div>
                <div class="mt-6">
                    <span class="p-float-label">
                        <InputText
                            v-model="agency.email"
                            class="w-full"
                            type="email"
                        />
                        <label for="email">Adresse email</label>
                    </span>
                </div>
                <div class="mt-6">
                    <span class="p-float-label">
                        <Password
                            v-model="agency.password"
                            :feedback="false"
                            class="w-full"
                            inputClass="w-full"
                            toggleMask
                        />
                        <label>Mot de passe</label>
                    </span>
                </div>
                <div class="mt-6">
                    <span class="p-float-label">
                        <InputNumber
                            v-model="agency.percentage"
                            class="w-full"
                        />
                        <label>Commission</label>
                    </span>
                </div>
                <div class="mt-6">
                    <input
                        accept="image/*"
                        class="w-full"
                        type="file"
                        @input="agency.logo = $event.target.files[0]"
                    />
                    <progress
                        v-if="agency.progress"
                        :value="agency.progress.percentage"
                        max="100"
                    >
                        {{ agency.progress.percentage }}%
                    </progress>
                </div>
                <div class="mt-6">
                    <Button
                        :loading="agency.processing"
                        class="w-full p-button-info"
                        icon="pi pi-check"
                        label="Modifier"
                        type="submit"
                    />
                </div>
            </form>
        </Dialog> -->

        <!-- agencies datatable-->
        <div class="mt-10 grid grid-cols-1">
            <DataTable
                v-model:expandedRows="expandedRows"
                v-model:filters="filters"
                :globalFilterFields="['user.name', 'location.name', 'phone']"
                :paginator="true"
                :rows="10"
                :rowsPerPageOptions="[10, 25, 50]"
                :value="agencies"
                class="p-datatable-customers"
                dataKey="id"
                filterDisplay="menu"
                responsiveLayout="scroll"
            >
                <template #header>
                    <div class="align-items-center flex justify-between">
                        <h5 class="m-0">Agencies</h5>
                        <Dropdown
                            v-model="location"
                            :filter="true"
                            :options="locations"
                            class="mb-4 w-64"
                            emptyFilterMessage="Aucune résultat"
                            emptyMessage="Aucune résultat"
                            optionLabel="name"
                            optionValue="id"
                            placeholder="Sélectionnez une ville"
                            @change="filterWithLocation"
                        />
                    </div>
                </template>
                <template #empty> Aucune agence.</template>
                <template #loading>
                    Chargement des données des agences. S'il vous plaît,
                    attendez.
                </template>
                <Column :expander="true" headerStyle="width: 3rem" />
                <Column bodyClass="capitalize" field="name" header="Nom" />
                <Column field="user.email" header="Adresse email" />
                <Column field="phone" header="Téléphone" />
                <Column
                    bodyClass="uppercase"
                    field="location.name"
                    header="Ville"
                />
                <Column header="Commission">
                    <template #body="{ data }">
                        {{ data.percentage }} %</template
                    >
                </Column>
                <Column header="Statut">
                    <template #body="{ data }">
                        <InputSwitch
                            v-model="data.user.is_active"
                            class=""
                            @change="
                                updateAccountStatus(
                                    data.id,
                                    data.user.is_active
                                )
                            "
                        />
                    </template>
                </Column>
                <Column header="Action">
                    <template #body="{ data }">
                        <Button
                            class="p-button-secondary"
                            icon="pi pi-pencil"
                            @click="showEditModal(data)"
                        ></Button>
                    </template>
                </Column>
                <template #expansion="{ data }">
                    <ul>
                        <li class="capitalize">
                            address:
                            <span class="font-semibold">{{
                                data.address
                            }}</span>
                        </li>
                        <li class="capitalize">
                            Affiliation date:
                            <span class="font-semibold">{{
                                data.affiliation_date
                            }}</span>
                        </li>
                    </ul>
                </template>
            </DataTable>
        </div>
    </Authenticated>
</template>

<style lang="scss" scoped>
::v-deep(.p-paginator) {
    .p-paginator-current {
        margin-left: auto;
    }
}

::v-deep(.p-datatable.p-datatable-customers) {
    .p-datatable-header {
        padding: 1rem;
        text-align: left;
        font-size: 1.5rem;
    }

    .p-paginator {
        padding: 1rem;
    }

    .p-datatable-thead > tr > th {
        text-align: left;
    }

    .p-datatable-tbody > tr > td {
        cursor: auto;
    }

    .p-dropdown-label:not(.p-placeholder) {
        text-transform: uppercase;
    }
}
</style>
