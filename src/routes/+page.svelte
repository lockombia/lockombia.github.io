<script lang="ts">
    import { messages, loadMessages } from "$lib/global";
    import { onMount } from "svelte";
    onMount(async () => {
        await loadMessages();
    });
    let last_message = $derived($messages[0]);
</script>

<div class="w-full h-full mt-12">
    <div
        class="flex w-[2000px] max-w-[50vw] h-20 mx-auto items-center justify-center mb-6 bg-black/50 shadow-md px-6 py-4 rounded"
    >
        <h1>En este momento</h1>
    </div>
</div>
<div class="w-full h-full mt-1">
    <div class="w-[90vw] h-50 mx-auto items-center mb-6 px-1 py-1 rounded">
        {#if last_message}
            <div
                class="bg-black/70 w-full h-[20%] rounded-t flex items-center justify-center px-4"
            >
                <h2 class="text-center font-bold">{last_message.subtitle}</h2>
            </div>
            <div
                class="bg-black/50 w-full h-[80%] rounded-b flex items-center justify-center px-4"
            >
                <h1 class="text-center break-words hyphens-auto">
                    {last_message.title}
                </h1>
            </div>
        {:else}
            <div
                class="bg-black/70 w-full h-full rounded flex items-center justify-center px-4"
            >
                <h3 class="text-center font-bold">Loading messages...</h3>
            </div>
        {/if}
    </div>
</div>


<!-- Global Title -->
<div class="w-full h-full mt-12">
  <div class="flex w-[2000px] max-w-[50vw] h-20 mx-auto items-center justify-center mb-6 bg-black/50 shadow-md px-6 py-4 rounded">
    <h1 class="font-bold">Direcciones</h1>
  </div>
</div>

<!-- 3 Column Scrollable Table -->
<div class="w-full mt-1 items-center justify-center">
  <div class="w-[90vw] mx-auto mb-6 px-1 py-1 ">
    <!-- Horizontal scrollable container -->
    <div class="overflow-x-auto ">
      <div class="flex gap-4" style="min-width: max-content;">
        
        <!-- Column 1: Fiesta (Viernes 26) -->
        <div class="bg-black/70 rounded" style="min-width: 200px; width:30vw; flex-shrink: 0;">
          <!-- Title Row -->
          <div class="h-20 flex items-center justify-center px-4 bg-black/80 rounded-t">
            <h2 class="text-center font-bold text-white">Fiesta (Viernes 26)</h2>
          </div>
          <!-- Map Row -->
          <div class="h-64 p-2 bg-black/50">
            <iframe 
              src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3976.8234573098805!2d-74.06541118255615!3d4.636068896641593!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x8e3f9b9860f8240b%3A0xd74b09e5f7d4143c!2sAc%C3%A1%20Parchamos!5e0!3m2!1sen!2sco!4v1695000000000!5m2!1sen!2sco"
              class="w-full h-full rounded"
              style="border:0;"
              loading="lazy"
              referrerpolicy="no-referrer-when-downgrade">
            </iframe>
          </div>
          <!-- Address Row -->
          <div class="h-16 flex items-center justify-center px-4 bg-black/60 rounded-b">
            <h2 class="text-center text-sm">Acá Parchamos (Cl. 49 #9-85)</h2>
          </div>
        </div>

        <!-- Column 2: Talleres (Sábado 27) -->
        <div class="bg-black/70 rounded" style="min-width: 200px; width:30vw; flex-shrink: 0;">
          <!-- Title Row -->
          <div class="h-20 flex items-center justify-center px-4 bg-black/80 rounded-t">
            <h2 class="text-center font-bold text-white">Talleres (Sábado 27)</h2>
          </div>
          <!-- Map Row -->
          <div class="h-64 p-2 bg-black/50">
            <iframe 
              src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3976.9514573098805!2d-74.09372468255615!3d4.609555496641593!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x8e3f998245256c21%3A0xdf61871be9631e81!2sBLOC%20Ricaurte%20Colsubsidio!5e0!3m2!1sen!2sco!4v1695000000000!5m2!1sen!2sco"
              class="w-full h-full rounded"
              style="border:0;"
              loading="lazy"
              referrerpolicy="no-referrer-when-downgrade">
            </iframe>
          </div>
          <!-- Address Row -->
          <div class="h-16 flex items-center justify-center px-4 bg-black/60 rounded-b">
            <h2 class="text-center text-sm">BLOC Ricaurte Colsubsidio (Cra 27 #11-54)</h2>
          </div>
        </div>

        <!-- Column 3: Batallas (Domingo 28) -->
        <div class="bg-black/70 rounded" style="min-width: 200px; width:30vw; flex-shrink: 0;">
          <!-- Title Row -->
          <div class="h-20 flex items-center justify-center px-4 bg-black/80 rounded-t">
            <h2 class="text-center font-bold text-white">Batallas (Domingo 28)</h2>
          </div>
          <!-- Map Row -->
          <div class="h-64 p-2 bg-black/50">
            <iframe 
              src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3976.7234573098805!2d-74.08060598255615!3d4.623112696641593!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x8e3f997f68a20ba5%3A0xf7fc126a9716bb1c!2sTeatro%20Colsubsidio!5e0!3m2!1sen!2sco!4v1695000000000!5m2!1sen!2sco"
              class="w-full h-full rounded"
              style="border:0;"
              loading="lazy"
              referrerpolicy="no-referrer-when-downgrade">
            </iframe>
          </div>
          <!-- Address Row -->
          <div class="h-16 flex items-center justify-center px-4 bg-black/60 rounded-b">
            <h2 class="text-center text-sm">Teatro Colsubsidio (Av. El Dorado #25-40)</h2>
          </div>
        </div>

      </div>
    </div>
  </div>
</div>

<!-- Global Title -->
<div class="w-full h-full mt-12">
  <div class="flex w-[2000px] max-w-[50vw] h-20 mx-auto items-center justify-center mb-6 bg-black/50 shadow-md px-6 py-4 rounded">
    <h1>Inversión</h1>
  </div>
</div>

<!-- Pricing Table -->
<div class="w-full mt-1">
  <div class="w-[90vw] max-w-2xl mx-auto mb-6 px-4 py-4">
    <div class="bg-black rounded-lg overflow-hidden shadow-lg">
      
      <!-- Workshop Internacional -->
      <div class="flex items-center justify-between p-4 border-b border-gray-700">
        <div class="flex items-center">
          <div class="w-0 h-0 border-l-[8px] border-l-yellow-400 border-t-[6px] border-t-transparent border-b-[6px] border-b-transparent mr-3"></div>
          <span class="text-white font-bold text-sm uppercase">WORKSHOP INTERNACIONAL</span>
        </div>
        <span class="text-yellow-400 font-bold">$135 MIL PESOS CO</span>
      </div>

      <!-- Workshop Nacional -->
      <div class="flex items-center justify-between p-4 border-b border-gray-700">
        <div class="flex items-center">
          <div class="w-0 h-0 border-l-[8px] border-l-yellow-400 border-t-[6px] border-t-transparent border-b-[6px] border-b-transparent mr-3"></div>
          <span class="text-white font-bold text-sm uppercase">WORKSHOP NACIONAL</span>
        </div>
        <span class="text-yellow-400 font-bold">$70 MIL PESOS CO</span>
      </div>

      <!-- 1 vs 1 Locking -->
      <div class="flex items-center justify-between p-4 border-b border-gray-700">
        <div class="flex items-center">
          <div class="w-0 h-0 border-l-[8px] border-l-yellow-400 border-t-[6px] border-t-transparent border-b-[6px] border-b-transparent mr-3"></div>
          <span class="text-white font-bold text-sm uppercase">1 VS 1 LOCKING</span>
        </div>
        <span class="text-yellow-400 font-bold">$45 MIL PESOS CO</span>
      </div>

      <!-- 2 vs 2 Open Styles -->
      <div class="flex items-center justify-between p-4 border-b border-gray-700">
        <div class="flex items-center">
          <div class="w-0 h-0 border-l-[8px] border-l-yellow-400 border-t-[6px] border-t-transparent border-b-[6px] border-b-transparent mr-3"></div>
          <span class="text-white font-bold text-sm uppercase">2 VS 2 OPEN STYLES</span>
        </div>
        <span class="text-yellow-400 font-bold">$80 MIL PESOS CO</span>
      </div>

      <!-- Público Batallas -->
      <div class="flex items-center justify-between p-4">
        <div class="flex items-center">
          <div class="w-0 h-0 border-l-[8px] border-l-yellow-400 border-t-[6px] border-t-transparent border-b-[6px] border-b-transparent mr-3"></div>
          <span class="text-white font-bold text-sm uppercase">PÚBLICO BATALLAS</span>
        </div>
        <span class="text-yellow-400 font-bold">$15 MIL PESOS CO</span>
      </div>

    </div>
  </div>
</div>


<!-- Global Title -->
<div class="w-full h-full mt-12">
  <div class="flex w-[2000px] max-w-[50vw] h-20 mx-auto items-center justify-center mb-6 bg-black/50 shadow-md px-6 py-4 rounded">
    <h1>Programación Workshops</h1>
  </div>
</div>

<!-- Schedule -->
<div class="w-full mt-1">
  <div class="w-[90vw] max-w-2xl mx-auto mb-6 px-4 py-4">
    <div class="bg-black rounded-lg overflow-hidden shadow-lg">
      
      <!-- Salsa -->
      <div class="flex items-center justify-between p-4 border-b border-gray-700">
        <div class="flex items-center">
          <div class="w-0 h-0 border-l-[8px] border-l-yellow-400 border-t-[6px] border-t-transparent border-b-[6px] border-b-transparent mr-3"></div>
          <span class="text-white font-bold text-sm uppercase">SALSA — IVONNE PULIDO</span>
        </div>
        <span class="text-yellow-400 font-bold">10:00 AM</span>
      </div>

      <!-- Locking -->
      <div class="flex items-center justify-between p-4 border-b border-gray-700">
        <div class="flex items-center">
          <div class="w-0 h-0 border-l-[8px] border-l-yellow-400 border-t-[6px] border-t-transparent border-b-[6px] border-b-transparent mr-3"></div>
          <span class="text-white font-bold text-sm uppercase">LOCKING — FLOCKEY</span>
        </div>
        <span class="text-yellow-400 font-bold">11:30 AM</span>
      </div>

      <!-- Almuerzo -->
      <div class="flex items-center justify-between p-4 border-b border-gray-700">
        <div class="flex items-center">
          <div class="w-0 h-0 border-l-[8px] border-l-yellow-400 border-t-[6px] border-t-transparent border-b-[6px] border-b-transparent mr-3"></div>
          <span class="text-white font-bold text-sm uppercase">ALMUERZO</span>
        </div>
        <span class="text-yellow-400 font-bold">1–2 PM</span>
      </div>

      <!-- Locking Coreográfico -->
      <div class="flex items-center justify-between p-4 border-b border-gray-700">
        <div class="flex items-center">
          <div class="w-0 h-0 border-l-[8px] border-l-yellow-400 border-t-[6px] border-t-transparent border-b-[6px] border-b-transparent mr-3"></div>
          <span class="text-white font-bold text-sm uppercase">LOCKING COREOGRÁFICO — FUNKY D</span>
        </div>
        <span class="text-yellow-400 font-bold">2:00 PM</span>
      </div>

      <!-- Taller Teórico -->
      <div class="flex items-center justify-between p-4">
        <div class="flex items-center">
          <div class="w-0 h-0 border-l-[8px] border-l-yellow-400 border-t-[6px] border-t-transparent border-b-[6px] border-b-transparent mr-3"></div>
          <span class="text-white font-bold text-sm uppercase">TALLER TEÓRICO — SCAYRA & PAULINA</span>
        </div>
        <span class="text-yellow-400 font-bold">3:30 PM</span>
      </div>

    </div>
  </div>
</div>


<!-- Global Title -->
<div class="w-full h-full mt-12">
  <div class="flex w-[2000px] max-w-[50vw] h-20 mx-auto items-center justify-center mb-6 bg-black/50 shadow-md px-6 py-4 rounded">
    <h1 class="font-bold text-black text-xl">Premiación</h1>
  </div>
</div>

<!-- 2 Column Scrollable Table -->
<div class="w-full mt-1">
  <div class="w-[90vw] mx-auto mb-6 px-1 py-1">
    <!-- Horizontal scrollable container -->
    <div class="overflow-x-auto">
      <div class="flex gap-4" style="min-width: max-content;">
        
        <!-- Column 1: LOCKING 1 VS 1 -->
        <div class="bg-black rounded" style="min-width: 300px; flex-shrink: 0; width: 50vw;">
          <!-- Title -->
          <div class="h-20 flex items-center justify-center px-4 bg-black rounded-t">
            <h2>LOCKING 1 VS 1</h2>
          </div>
          
          <!-- 1er lugar -->
          <div class="bg-gray-900 px-4 py-3">
            <h3 class="text-center font-bold text-black text-base">1er lugar</h3>
            <div class="bg-black font-bold text-center py-2 px-4 rounded my-2">
              $500.000 MIL PESOS CO
            </div>
            <div class="text-black text-sm text-center space-y-1">
              <p>Full pass Pink Funky Weekend 2026 Toulouse Francia</p>
              <p>Full pass y pase al top stop and lock Monterrey México 2025</p>
              <p>Full pass y pase al top de Seminario Locking 2026 Lima Perú</p>
              <p>Arte de patrocinadores</p>
            </div>
          </div>
          
          <!-- 2do lugar -->
          <div class="bg-gray-800 px-4 py-3 rounded-b">
            <h3 class="text-center font-bold text-black text-base">2do lugar</h3>
            <div class="bg-black text-yellow-400 font-bold text-center py-2 px-4 rounded my-2">
              $300.000 MIL PESOS CO
            </div>
            <div class="text-black text-sm text-center space-y-1">
              <p>Full pass Lock Latino Cdmx México 2026</p>
              <p>Beca 4 clases AcroMove</p>
              <p>Arte de patrocinadores</p>
            </div>
          </div>
        </div>

        <!-- Column 2: 2 VS 2 OPEN STYLES -->
        <div class="bg-black rounded" style="min-width: 300px; flex-shrink: 0; width: 50vw;">
          <!-- Title -->
          <div class="h-20 flex items-center justify-center px-4 bg-black rounded-t">
            <h2 class="text-center font-bold text-black text-lg">2 VS 2 OPEN STYLES</h2>
          </div>
          
          <!-- 1er lugar -->
          <div class="bg-gray-900 px-4 py-3">
            <h3 class="text-center font-bold text-black text-base">1er lugar</h3>
            <div class="bg-black font-bold text-center py-2 px-4 rounded my-2">
              $500.000 MIL PESOS CO
            </div>
            <div class="text-black text-sm text-center space-y-1">
              <p>1 Full pass chill In da hood 2025</p>
              <p>1 Full pass para Bombohop 2026</p>
              <p>2 Full pass para Raíz en tribu 2026 y cupo al top</p>
              <p>Arte de patrocinadores</p>
            </div>
          </div>
          
          <!-- 2do lugar -->
          <div class="bg-gray-800 px-4 py-3 rounded-b">
            <h3 class="text-center font-bold text-black text-base">2do lugar</h3>
            <div class="bg-black font-bold text-center py-2 px-4 rounded my-2">
              $300.000 MIL PESOS CO
            </div>
            <div class="text-black text-sm text-center space-y-1">
              <p>Arte de patrocinadores</p>
            </div>
          </div>
        </div>

      </div>
    </div>
  </div>
</div>