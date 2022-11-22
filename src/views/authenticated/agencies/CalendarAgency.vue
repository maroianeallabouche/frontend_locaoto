<template>
    <Authenticated>
        <div>
            <FullCalendar :events="events" :options="options" />
        </div>
    </Authenticated>
</template>

<script>
import FullCalendar from "@fullcalendar/vue3";
import dayGridPlugin from "@fullcalendar/daygrid";
import timeGridPlugin from "@fullcalendar/timegrid";
import interactionPlugin from "@fullcalendar/interaction";
import EventService from "./EventService";

export default {
    components: {
        FullCalendar,
    },
    data() {
        return {
            options: {
                plugins: [dayGridPlugin, timeGridPlugin, interactionPlugin],
                initialDate: new Date(),
                headerToolbar: {
                    left: "prev,next today",
                    center: "title",
                    right: "dayGridMonth,timeGridWeek,timeGridDay",
                },
                editable: true,
                selectable: true,
                selectMirror: true,
                dayMaxEvents: true,
            },
            events: null,
        };
    },
    eventService: null,
    created() {
        this.eventService = new EventService();
    },
    mounted() {
        this.eventService.getEvents().then((data) => (this.events = data));
    },
};
</script>

<style scoped>
@media screen and (max-width: 960px) {
    ::v-deep(.fc-header-toolbar) {
        display: flex;
        flex-wrap: wrap;
    }
}
</style>
