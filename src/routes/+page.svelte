<script lang="ts">
    import { Card } from "flowbite-svelte";
    import {
        Table,
        TableBody,
        TableBodyCell,
        TableBodyRow,
        TableHead,
        TableHeadCell,
    } from "flowbite-svelte";
</script>

<!-- <div
    class="my-7 mx-auto w-fit rounded-xl backdrop-blur-md bg-white/50 px-6 py-4 shadow-md border-4 border-primary-200"
>
    <h1>Inicio</h1>
</div> -->
<div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-0 px-0">
    <div  class="w-full mt-12">
        <div 
            class="flex w-[90%] h-20 mx-auto items-center justify-center mb-6 bg-black/40 shadow-md px-6 py-4 border-0 border-primary-200 rounded"
        >
            <h1 class="text-2xl truncate">Panel de Jueces</h1>
        </div>
        <div class="overflow-x-hidden">
            <div class="flex gap-4 px-4 w-max scroll-auto-x">
                <Card
                    class="min-w-[280px] max-w-[320px]"
                    img="assets/IMG_4227.JPG"
                >
                    <h5 class="text-lg font-semibold text-center">TayTay</h5>
                </Card>
                <Card
                    class="min-w-[280px] max-w-[320px]"
                    img="assets/IMG_4225.JPG"
                >
                    <h5 class="text-lg font-semibold text-center">Mancho</h5>
                </Card>
                <Card
                    class="min-w-[280px] max-w-[320px]"
                    img="assets/IMG_4226.JPG"
                >
                    <h5 class="text-lg font-semibold text-center">
                        Ricky Rulez
                    </h5>
                </Card>
                <Card
                    class="min-w-[280px] max-w-[320px]"
                    img="assets/IMG_4227.JPG"
                >
                    <h5 class="text-lg font-semibold text-center">TayTay</h5>
                </Card>
                <Card
                    class="min-w-[280px] max-w-[320px]"
                    img="assets/IMG_4225.JPG"
                >
                    <h5 class="text-lg font-semibold text-center">Mancho</h5>
                </Card>
                <Card
                    class="min-w-[280px] max-w-[320px]"
                    img="assets/IMG_4226.JPG"
                >
                    <h5 class="text-lg font-semibold text-center">
                        Ricky Rulez
                    </h5>
                </Card>
            </div>
        </div>
    </div>

    <div class="w-full mt-12">
        <div
            class="flex w-[90%] h-20 mx-auto items-center justify-center mb-6 bg-black/40 shadow-md px-6 py-4 border-0 border-primary-200 rounded"
        >
            <h1>Cronograma</h1>
        </div>
        <div class="flex justify-center">
            <Table
                class="w-5/6 max-w-4xl h-full rounded-md shadow-md mb-8 :divide-y-0 "
            >
                <TableHead class="bg-white/60 hover:underline">
                    <TableHeadCell>Evento</TableHeadCell>
                    <TableHeadCell>Hora</TableHeadCell>
                </TableHead>
                <TableBody>
                    <TableBodyRow class="bg-white/80 hover:underline border-0">
                        <TableBodyCell>Inscripción</TableBodyCell>
                        <TableBodyCell>1 PM</TableBodyCell>
                    </TableBodyRow>
                    <TableBodyRow class="bg-white/60 hover:underline border-0">
                        <TableBodyCell>Filtros</TableBodyCell>
                        <TableBodyCell>2 PM</TableBodyCell>
                    </TableBodyRow>
                    <TableBodyRow class="bg-white/80 hover:underline border-0">
                        <TableBodyCell>Semifinales</TableBodyCell>
                        <TableBodyCell>5 PM</TableBodyCell>
                    </TableBodyRow>
                </TableBody>
            </Table>
        </div>
    </div>

    <div class="w-full mt-12">
        <div
            class="flex w-[90%] h-20 mx-auto items-center justify-center mb-6 bg-black/40 shadow-md px-6 py-4 border-0 border-primary-200 rounded"
        >
            <h1>Cómo llegar</h1>
        </div>

        <div class="flex justify-center">
            <iframe
                title="Teatro El Espacio"
                class="w-5/6 max-w-4xl h-96 rounded-md shadow-md mb-8"
                loading="lazy"
                allowfullscreen
                referrerpolicy="no-referrer-when-downgrade"
                src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3976.8091390919276!2d-74.0709593!3d4.6111872!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x8e3f9999514c6f5d%3A0x4cf4ca8276154ff7!2s%22El%20Espacio%22%20Teatro%20Occidente!5e0!3m2!1ses!2sco!4v1721745600000!5m2!1ses!2sco"
            >
            </iframe>
        </div>
    </div>
</div>

<style>
    @keyframes scrollX {
        0% {
            transform: translateX(0);
        }
        100% {
            transform: translateX(-50%);
        }
    }

    .scroll-auto-x {
        animation: scrollX 45s linear infinite;
    }
</style>
