<script>
  import { T, useTask } from '@threlte/core'
  import { interactivity } from '@threlte/extras'
  import { spring } from 'svelte/motion' 

  interactivity() //aanroepen van interactive functies
  const scale = spring(1) //schaling van animatie 
  let rotation = 0 //rotation functie wordt ingezet
  useTask((delta) => { // delta is tijdsinterval
    rotation += delta //rotation wordt geanimeerd met tijd
  })
</script>

<T.PerspectiveCamera 
  makeDefault 
  position={[10, 10, 10]}
  on:create={({ ref }) => {
    ref.lookAt(0, 1, 0)
    // T.PerspectiveCamera is the 3d camera, makeDefault should be used for rendering
  }}
  
/>

<T.DirectionalLight
  position={[0, 10, 10]} 
  castShadow
/>


<T.Mesh
  rotation.y={rotation}
  position.y={1}
  scale={$scale}
  on:pointerenter={() => scale.set(1.5)}
  on:pointerleave={() => scale.set(1)}
  castShadow
>
  <T.BoxGeometry args={[1, 2, 1]} />
  <T.MeshStandardMaterial color="hotpink" />
</T.Mesh>
<T.Mesh
  rotation.x={-Math.PI / 2}
  receiveShadow
>
  <T.CircleGeometry args={[4, 40]} />
  <T.MeshStandardMaterial color="white" />
</T.Mesh>
  