<script lang="ts">
    async function getOwner() {
        const res = await fetch("http://127.0.0.1:9999/tracer/owner")
        const owner = await res.json()

        console.log('Owner is', owner)

        if (res.ok){
            return owner;
        }
        else {
            throw new Error(owner)
        }
    }
</script>