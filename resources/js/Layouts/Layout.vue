<template>
    <div id="main-wrapper">
        <div id="sidebar" class="min-w-[500px] bg-gradient-to-b from-gray-700 to-gray-500 flex flex-col items-center">
            <div id="branding">
                <img src="https://media1.tenor.com/m/xlFZTbLqs20AAAAd/itachi.gif" alt="">
            </div>

            <div>
                <h1 class="mt-[10%] fw-bold">Mathew Jerome Carillo<br> <em>(kuan)</em></h1>
                <h4>BSIT-3</h4>
            </div>

            <div class="mt-[20%]">
                <Link href="/projects" class="button-53"> Projects</Link>
                <Link href="/landing" class="button-about-me">About Me</Link>
            </div>
        </div>
        <div id="content" class="flex flex-col flex-1">
            <div class="flex-1 p-0">
                <Transition name="page-trans" mode="out-in">
                    <div>
                        <slot />
                    </div>
                </Transition>
            </div>
            <!-- <footer class="py-4 text-gray-600 text-center bg-white" style="font-style: italic;">
                Inertia Final Project 2024
            </footer> -->
        </div>
    </div>
</template>

<script setup>
    import { Link } from "@inertiajs/vue3";
</script>

<style scoped>
#sidebar {
    min-width: 350px;
    background-color: #d5eae6;
    display: flex;
    flex-direction: column;
    align-items: center;
}
.button-53 {
    background-color: #3d52b1;
    border: 0 solid #E5E7EB;
    box-sizing: border-box;
    color: #000000;
    display: flex;
    font-family: ui-sans-serif,system-ui,-apple-system,system-ui,"Segoe UI",Roboto,"Helvetica Neue",Arial,"Noto Sans",sans-serif,"Apple Color Emoji","Segoe UI Emoji","Segoe UI Symbol","Noto Color Emoji";
    font-size: 1rem;
    margin-bottom: 20px;
    font-weight: 700;
    justify-content: center;
    line-height: 1.75rem;
    padding: .75rem 1.65rem;
    position: relative;
    text-align: center;
    text-decoration: none #000000 solid;
    text-decoration-thickness: auto;
    width: 100%;
    max-width: 460px;
    position: relative;
    cursor: pointer;
    transform: rotate(-2deg);
    user-select: none;
    -webkit-user-select: none;
    touch-action: manipulation;
    border-radius: 5px;
    transition: all 0.3s ease;
}

.button-53:focus {
    outline: 0;
}

.button-53:after {
    content: '';
    position: absolute;
    border: 1px solid #000000;
    bottom: 4px;
    left: 4px;
    width: calc(100% - 1px);
    height: calc(100% - 1px);
}

.button-53:hover:after {
    bottom: 2px;
    left: 2px;
}

@media (min-width: 768px) {
    .button-53 {
        padding: .75rem 3rem;
        font-size: 1.25rem;
    }
}

.button-about-me {
    background-color: #0bdaad;
    border: 1 solid #E5E7EB;
    box-sizing: border-box;
    color: #000000;
    display: flex;
    font-family: ui-sans-serif,system-ui,-apple-system,system-ui,"Segoe UI",Roboto,"Helvetica Neue",Arial,"Noto Sans",sans-serif,"Apple Color Emoji","Segoe UI Emoji","Segoe UI Symbol","Noto Color Emoji";
    font-size: 1rem;
    font-weight: 700;
    justify-content: center;
    line-height: 1.75rem;
    padding: .75rem 1.65rem;
    position: relative;
    text-align: center;
    text-decoration: none #000000 solid;
    text-decoration-thickness: auto;
    width: 100%;
    max-width: 460px;
    position: relative;
    cursor: pointer;
    transform: rotate(-2deg);
    user-select: none;
    -webkit-user-select: none;
    touch-action: manipulation;
    border-radius: 5px;
    transition: all 0.3s ease;
}

.button-about-me:focus {
    outline: 0;
}

.button-about-me:after {
    content: '';
    position: absolute;
    border: 1px solid #000000;
    bottom: 4px;
    left: 4px;
    width: calc(100% - 1px);
    height: calc(100% - 1px);
}

.button-about-me:hover:after {
    bottom: 2px;
    left: 2px;
}

h4 {
    margin-top: 5%;
    font-size: 30px;
    color: black;
    /* font-size: 25px; */
}

h1 {
    font-size: 30px;
    color: black;
}

#main-wrapper {
    min-height: 100vh;
    display: flex;
    background-color: #5f6b79;
    min-height: 100vh;
    width: 100%;
}

#branding img {
    width: 200px;
    height: 200px;
    border-radius: 150px;
    margin-top: 24px;
}
</style>
