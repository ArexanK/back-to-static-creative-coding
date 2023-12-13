<script>
  import BtnPrimary from "$lib/atoms/BtnPrimary.svelte";

    // import '../lib/styles/fonts';
    import { Header } from "../lib/index";
    import App from './App.svelte'
</script>

<Header />

<div>
	<App />
</div>






<slot />



<style>



	div {
		position: absolute;
		height: 100%;
		width: 100%;
	}

    :global(*){
        box-sizing: border-box;
        text-decoration: none;
        list-style: none;
        margin: 0;
        padding: 0;
        font-family: var(--Apercu-font);
    }

    /* Color variable */

    :global(:root){

        --Bg-Dark-Blue: #051d1d;
        --Bg-Fern-Green: #4F7942;

        --Yellow-Primary: #FFDA1D;
        --Blue-Secondary: #3DBAE1;

        --White: #FFFFFF;
        --Black: #000;

        --Apercu-Font: 'Apercu pro', sans-serif;
        --Paragraph-Font: 'Jubilat', serif;
        --Header-Font: 'Kirang Haerang', sans-serif;
        --McKloud-Font: 'Mckloud'

    }

    :global(body) {
        background-color: var(--Bg-Dark-Blue);
        color: var(--White);
        width: 100%;
        height: 100vh;
        overflow: hidden;
        overflow-y: scroll;
    }

    :global(h1){
        font-family: var(--Header-Font);
        font-size: 4em;
        padding: .5em;
        color: var(--Yellow-Primary);
    }

    :global(h2){
        font-family: var( --Paragraph-Font);
    }

</style>