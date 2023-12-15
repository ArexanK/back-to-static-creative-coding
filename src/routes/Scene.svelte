<script>
  import { T, useTask } from '@threlte/core'
  import { OrbitControls, interactivity } from '@threlte/extras'
  import * as Three from 'three'

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
}}
/>
<T.Mesh
rotation.y={rotation}
position.y={1}
scale={$scale}
on:pointerenter={() => scale.set(1.5)}
on:pointerleave={() => scale.set(1)}
>
<T.BoxGeometry args={[3, 3, 3]} />
<T.MeshBasicMaterial color= '#3DBAE1'/>

</T.Mesh>

