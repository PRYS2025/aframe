<script src="https://raw.githack.com/AR-js-org/AR.js/master/aframe/build/aframe-ar.js"></script>
<a-scene embedded arjs>
  <!-- Aquí irán tus objetos 3D y elementos interactivos -->
  
  <!-- Marcador que activará tu contenido RA -->
  <a-marker preset="hiro">
    <!-- Contenido que aparecerá sobre el marcador -->
    <a-box position="0 0.5 0" material="color: red;"></a-box>
  </a-marker>
  
  <!-- Cámara necesaria para la experiencia -->
  <a-entity camera></a-entity>
</a-scene>
<a-marker preset="hiro">
  <!-- Modelo 3D del modelo ADDIE -->
  <a-entity 
    position="0 0 0" 
    scale="0.5 0.5 0.5" 
    rotation="-90 0 0" 
    gltf-model="url(ruta-a-tu-modelo/addie-model.glb)">
  </a-entity>
</a-marker>
AFRAME.registerComponent('rotate-on-click', {
  init: function () {
    this.el.addEventListener('click', function () {
      this.object3D.rotation.y += Math.PI/4;
    });
  }
});
<a-entity gltf-model="url(model.glb)" rotate-on-click></a-entity>



