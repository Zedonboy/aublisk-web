<script>
    import "../app.css"
    import 'flowbite';
    import { dev } from '$app/environment';
    import { inject } from '@vercel/analytics';

    import {onMount} from "svelte"
    inject({ mode: dev ? 'development' : 'production' });
    onMount(() => {
		(function (w, d, e, u, f, l, n) {
			w[f] = w[f] || function () {
				(w[f].q = w[f].q || [])
				.push(arguments);
			}, l = d.createElement(e), l.async = 1, l.src = u,
			n = d.getElementsByTagName(e)[0], n.parentNode.insertBefore(l, n);
		})
			(window, document, 'script', 'https://assets.mailerlite.com/js/universal.js', 'ml');
		ml('account', '1027036');
    })
    
</script>
<slot/>