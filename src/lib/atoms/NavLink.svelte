<script>
	export let href, title;
</script>


	<a class="nav-link" {href}>{title}</a>


<style>

    a {
        color: var(--White);
        font-family: var(--Mckloud-font);
        text-transform: uppercase ;
        font-size: 2em;
        display: inline-block;

        padding: 1.2em 2em;
        text-decoration: none;
        text-align: center;
    }

    a:hover {
        color: var(--Yellow-Primary);
    }

    @media (min-width: 48em) {


        a {
            font-size: 1em;
        }

    }


</style>