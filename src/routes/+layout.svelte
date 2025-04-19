<script lang="ts">
	let { children } = $props();
    import "../app.css";
</script>

<div class="container">
    <nav>
        <ul>
            <li><a href="/">Home</a></li>
        </ul>
        <ul>
            <li><a href="/about">About</a></li>
            <li><a href="/api">API</a></li>
            <li><a href="/blog/hello-world">Blog</a></li>
            <li><a href="/settings">Settings</a></li>
        </ul>
    </nav>
    
    {@render children()}

    <button class="bottom-center" style="border-radius:5rem; padding: 1.5rem 2rem">+</button>
</div>
