<template>
    <Header />
    <!-- Meilleurs prix garantis -->
    <div class="md:px-24 md:pb-10 mb-3 pb-5 px-8 bg-gray-200">
        <div class="md:py-10 py-5">
            <h1 class="md:text-2xl text-lg text-gray-600 font-bold text-center">
                Meilleurs prix garantis pour vous !
            </h1>
        </div>
        <div
            class="md:flex md:justify-between md:ml-0 ml-10 md:items-center grid grid-cols-3 gab-x-8"
        >
            <img
                src="../../assets/images/images/alfa.png"
                class="md:w-20 md:h-20 w-16 h-16"
                alt=""
                srcset=""
            />
            <img
                src="../../assets/images/images/audi.png"
                class="md:w-28 md:h-20 w-16 h-16 md:flex hidden"
                alt=""
                srcset=""
            />
            <img
                src="../../assets/images/images/chev.png"
                class="md:w-20 md:h-20 w-16 h-16 md:flex hidden"
                alt=""
                srcset=""
            />
            <img
                src="../../assets/images/images/bmw.png"
                class="md:w-20 md:h-20 w-16 h-16"
                alt=""
                srcset=""
            />
            <img
                src="../../assets/images/images/ford.png"
                class="md:w-20 md:h-20 w-16 h-16 md:flex hidden"
                alt=""
                srcset=""
            />
            <img
                src="../../assets/images/images/ben.png"
                class="md:w-20 md:h-20 w-16 h-16"
                alt=""
                srcset=""
            />
        </div>
    </div>
    <!-- Comment ça fonctionne ? -->
    <div class="md:mx-24 mx-8">
        <div class="py-10">
            <h1
                class="md:text-4xl md:text-left text-xl text-center text-blue-800 font-bold"
            >
                Comment ça fonctionne ?
            </h1>
            <div
                class="md:w-20 h-2 w-16 bg-blue-800 rounded-full mx-auto md:mx-0 mt-3"
            ></div>
        </div>
        <div class="md:flex md:justify-between">
            <div class="text-center md:w-1/5 w-full">
                <h1 class="text-orange-600 font-bold text-2xl">
                    1. <span class="text-xl">Choisir</span>
                </h1>
                <p class="font-semibold text-gray-800 mt-2">
                    le lieu, les dates et les heures de votre prochaine
                    location.
                </p>
            </div>
            <div class="text-center md:w-1/5 w-full md:mt-0 mt-4">
                <h1 class="text-orange-600 font-bold text-2xl">
                    2. <span class="text-xl">Comparez</span>
                </h1>
                <p class="font-semibold text-gray-800 mt-2">
                    des centaines d’offres et choisissez la mieux adaptée à vos
                    besoins.
                </p>
            </div>
            <div class="text-center md:w-1/5 w-full md:mt-0 mt-4">
                <h1 class="text-orange-600 font-bold text-2xl">
                    3. <span class="text-xl">Réservez</span>
                </h1>
                <p class="font-semibold text-gray-800 mt-2">
                    Contacter notre equipe pour reserver votre voiture.
                </p>
            </div>
            <div class="text-center md:w-1/5 w-full md:mt-0 mt-4">
                <h1 class="text-orange-600 font-bold text-2xl">
                    4. <span class="text-xl">Confirmer</span>
                </h1>
                <p class="font-semibold text-gray-800 mt-2">
                    Patienter , pour nous confirmons votre resérvation.
                </p>
            </div>
        </div>
        <div class="py-8">
            <h1 class="text-2xl text-gray-600 font-bold text-center">Ou</h1>
            <h1 class="text-gray-500 font-bold text-center">
                Confiez-nous votre réservation par téléphone
            </h1>
            <h1 class="text-2xl text-orange-600 font-bold text-center">
                <a href="tel:+212707786109">+212 7-07 78 61 09</a>
            </h1>
            <h1 class="text-2xl text-orange-600 font-bold text-center">
                <a href="tel:+212661839986">+212 6-61 83 99 86</a>
            </h1>
        </div>
    </div>
    <!--Pourquoi locaoto.ma ? -->
    <div class="md:mx-24 mx-8 mb-4">
        <div class="py-10">
            <h1
                class="md:text-4xl md:text-left text-xl text-center text-blue-800 font-bold"
            >
                Pourquoi locaoto.ma ?
            </h1>
            <div
                class="md:w-20 h-2 w-16 bg-blue-800 rounded-full mx-auto md:mx-0 mt-3"
            ></div>
        </div>
        <div
            class="md:flex md:justify-around grid grid-col-1 place-content-center md:py-4 py-3 md:mx-36"
        >
            <div
                class="flex items-center rounded-xl hover:shadow-xl tarnsition-all duration-100 border-2 border-gray-200 md:p-5 p-3 md:w-96 w-72"
            >
                <img
                    src="../../assets/images/images/credit-card.png"
                    class="md:w-12 md:h-12 w-10 h-10"
                    alt=""
                    srcset=""
                />
                <div class="ml-4">
                    <h1 class="text-gray-600 font-bold md:text-xl text-lg">
                        Paiement sécurisé
                    </h1>
                    <p class="text-gray-500 md:text-sm text-xs">
                        Transactions et données sécurisées et chiffrées.
                    </p>
                </div>
            </div>
            <div
                class="flex items-center rounded-xl hover:shadow-xl tarnsition-all duration-100 border-2 border-gray-200 md:p-5 p-3 md:w-96 w-72 md:mt-0 mt-4"
            >
                <img
                    src="../../assets/images/images/price-tag.png"
                    class="md:w-12 md:h-12 w-10 h-10"
                    alt=""
                    srcset=""
                />
                <div class="ml-4">
                    <h1 class="text-gray-600 font-bold md:text-xl text-lg">
                        Prix transparents
                    </h1>
                    <p class="text-gray-500 md:text-sm text-xs">
                        Payez et conduisez ce que vous réservez. Aucune surprise
                        !
                    </p>
                </div>
            </div>
        </div>
        <div
            class="md:flex md:justify-around grid grid-col-1 place-content-center md:py-4 py-1 md:mx-36"
        >
            <div
                class="flex items-center rounded-xl hover:shadow-xl tarnsition-all duration-100 border-2 border-gray-200 md:p-5 p-3 md:w-96 w-72"
            >
                <img
                    src="../../assets/images/images/call-center.png"
                    class="md:w-12 md:h-12 w-10 h-10"
                    alt=""
                    srcset=""
                />
                <div class="ml-4">
                    <h1 class="text-gray-600 font-bold md:text-xl text-lg">
                        Support
                    </h1>
                    <p class="text-gray-500 md:text-sm text-xs">
                        Equipe Locaoto.ma disponible <br />
                        7j/7
                    </p>
                </div>
            </div>
            <div
                class="flex items-center rounded-xl hover:shadow-xl tarnsition-all duration-100 border-2 border-gray-200 md:p-5 p-3 md:w-96 w-72 md:mt-0 mt-4"
            >
                <img
                    src="../../assets/images/images/deposit.png"
                    class="md:w-12 md:h-12 w-10 h-10"
                    alt=""
                    srcset=""
                />
                <div class="ml-4">
                    <h1 class="text-gray-600 font-bold md:text-xl text-lg">
                        Caution à petit prix
                    </h1>
                    <p class="text-gray-500 md:text-sm text-xs">
                        Cautions abordables avec facilités de dépôt
                        intéressantes.
                    </p>
                </div>
            </div>
        </div>
    </div>
    <!-- Top destination  -->
    <div class="md:mx-24 mx-8 md:mb-4">
        <div class="py-16">
            <h1
                class="md:text-4xl md:text-left text-xl text-center text-blue-800 font-bold"
            >
                Top destinations
            </h1>
            <div
                class="md:w-20 h-2 w-16 bg-blue-800 rounded-full mx-auto md:mx-0 mt-3"
            ></div>
        </div>
        <div class="md:flex md:justify-around">
            <div
                class="relative overflow-hidden md:w-1/4 w-full md:mb-0 mb-4 h-80 bg-cover bg-no-repeat bg-center rounded-xl"
                style="
                    background-image: url('../../assets/images/images/rabat.jpg');
                "
            >
                <div
                    class="absolute bg-slate-900 w-full h-60 hover:top-0 top-[-160px] tarnsition-all duration-500 rounded-t-xl opacity-95"
                >
                    <div class="h-2/3 pt-4">
                        <a
                            href="#"
                            class="buttom-0 text-white ml-3 font-semibold text-xl block"
                            >link</a
                        >
                        <a
                            href="#"
                            class="buttom-0 text-white ml-3 font-semibold text-xl block"
                            >link</a
                        >
                        <a
                            href="#"
                            class="buttom-0 text-white ml-3 font-semibold text-xl block"
                            >link</a
                        >
                        <a
                            href="#"
                            class="buttom-0 text-white ml-3 font-semibold text-xl block"
                            >link</a
                        >
                    </div>
                    <div class="h-1/3 py-6">
                        <h1
                            class="buttom-0 text-white text-center font-bold text-2xl opacity-100"
                        >
                            Rabat
                        </h1>
                    </div>
                </div>
            </div>
            <div
                class="relative overflow-hidden md:w-1/4 w-full md:mb-0 mb-4 h-80 bg-cover bg-no-repeat bg-center rounded-xl"
                style="
                    background-image: url('../../assets/images/images/casa.jpg');
                "
            >
                <div
                    class="absolute bg-slate-900 w-full h-60 hover:top-0 top-[-160px] tarnsition-all duration-500 rounded-t-xl opacity-95"
                >
                    <div class="h-2/3 pt-4">
                        <a
                            href="#"
                            class="buttom-0 text-white ml-3 font-semibold text-xl block"
                            >link</a
                        >
                        <a
                            href="#"
                            class="buttom-0 text-white ml-3 font-semibold text-xl block"
                            >link</a
                        >
                        <a
                            href="#"
                            class="buttom-0 text-white ml-3 font-semibold text-xl block"
                            >link</a
                        >
                        <a
                            href="#"
                            class="buttom-0 text-white ml-3 font-semibold text-xl block"
                            >link</a
                        >
                    </div>
                    <div class="h-1/3 py-6">
                        <h1
                            class="buttom-0 text-white text-center font-bold text-2xl"
                        >
                            Casablanca
                        </h1>
                    </div>
                </div>
            </div>
            <div
                class="relative overflow-hidden md:w-1/4 w-full h-80 bg-cover bg-no-repeat bg-center rounded-xl"
                style="
                    background-image: url('../../assets/images/images/marrakesh.jpg');
                "
            >
                <div
                    class="absolute bg-slate-900 w-full h-60 hover:top-0 top-[-160px] tarnsition-all duration-500 rounded-t-xl opacity-95"
                >
                    <div class="h-2/3 pt-4">
                        <a
                            href="#"
                            class="buttom-0 text-white ml-3 font-semibold text-xl block"
                            >link</a
                        >
                        <a
                            href="#"
                            class="buttom-0 text-white ml-3 font-semibold text-xl block"
                            >link</a
                        >
                        <a
                            href="#"
                            class="buttom-0 text-white ml-3 font-semibold text-xl block"
                            >link</a
                        >
                        <a
                            href="#"
                            class="buttom-0 text-white ml-3 font-semibold text-xl block"
                            >link</a
                        >
                    </div>
                    <div class="h-1/3 py-6">
                        <h1
                            class="buttom-0 text-white text-center font-bold text-2xl"
                        >
                            Marrakesh
                        </h1>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <!-- footer -->
    <!-- nos partenaire -->
    <div class="md:mx-24 mx-8">
        <div class="py-3">
            <div class="py-10">
                <h1
                    class="md:text-2xl text-xl text-gray-600 font-bold text-center"
                >
                    Nos partenaires
                </h1>
            </div>
            <div class="md:ml-16 ml-4">
                <section class="customer-logos slider flex justify-around">
                    <div class="slide">
                        <img
                            src="../../assets/images/images2/adidas.png"
                            style="width: 100px"
                            alt="logo"
                        />
                    </div>
                    <div class="slide">
                        <img
                            src="../../assets/images/images2/facebook.png"
                            style="width: 100px"
                            alt="logo"
                        />
                    </div>
                    <div class="slide">
                        <img
                            src="../../assets/images/images2/google.png"
                            style="width: 100px"
                            alt="logo"
                        />
                    </div>
                    <div class="slide">
                        <img
                            src="../../assets/images/images2/instagram.png"
                            style="width: 100px"
                            alt="logo"
                        />
                    </div>
                    <div class="slide">
                        <img
                            src="../../assets/images/images2/nike.png"
                            style="width: 100px"
                            alt="logo"
                        />
                    </div>
                    <div class="slide">
                        <img
                            src="../../assets/images/images2/twitter.png"
                            style="width: 100px"
                            alt="logo"
                        />
                    </div>
                    <div class="slide">
                        <img
                            src="../../assets/images/images2/uber.png"
                            style="width: 100px"
                            alt="logo"
                        />
                    </div>
                    <div class="slide">
                        <img
                            src="../../assets/images/images2/youtube.png"
                            style="width: 100px"
                            alt="logo"
                        />
                    </div>
                </section>
                <!-- <script>
                    $(document).ready(function () {
                        $('.customer-logos').slick({
                            slidesToShow: 7,
                            slidesToScroll: 1,
                            autoplay: true,
                            autoplaySpeed: 1000,
                            arrows: false,
                            dots: false,
                            pauseOnHover: false,
                            responsive: [{
                                breakpoint: 600,
                                settings: {
                                    slidesToShow: 3
                                }
                            }, {
                                breakpoint: 400,
                                settings: {
                                    slidesToShow: 2
                                }
                            }]
                        });
                    });
                </script> -->
            </div>
        </div>
        <div class="flex my-12">
            <div
                class="md:w-1/2 w-full bg-blue-900 md:rounded-tl-2xl md:rounded-bl-2xl md:rounded-br-none md:rounded-tr-none rounded-xl md:pb-0 pb-10"
            >
                <div class="px-12 py-12">
                    <h1 class="md:text-4xl text-3xl text-white font-bold">
                        Devenir partenaire ?
                    </h1>
                    <div
                        class="w-20 h-2 bg-white rounded-full md:mt-3 mt-5"
                    ></div>
                </div>
                <div
                    class="px-12 text-white font-semibold md:text-left text-justify"
                >
                    <p>
                        Vous possédez une agence de location de voiture au Maroc
                        et vous souhaitez exposer votre flotte sur la centrale
                        de réservation Locaoto.ma, vous êtes au bon endroit !
                    </p>
                </div>
                <div class="px-12 mt-10">
                    <button
                        class="md:w-52 w-full bg-orange-600 text-white font-semibold text-lg py-2 px-6 rounded-xl"
                    >
                        Rejoignez-nous
                    </button>
                </div>
            </div>
            <div
                class="md:inline-flex hidden w-1/2 h-96 bg-cover bg-no-repeat bg-center rounded-tr-2xl rounded-br-2xl"
                style="
                    background-image: url('../../assets/images/images/bg2.jpg');
                "
            ></div>
        </div>
    </div>
    <Footer />
</template>

<script>
import Header from "./Header.vue";
import Footer from "./Footer.vue";
export default {
    components: {
        Header,
        Footer,
    },
};
</script>

<style></style>
