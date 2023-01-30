<script>
    // "Reusable components"
    import Book from './Book.svelte'
    import Button from './Button.svelte'
    
    let title = '';
    let price = 0;
    let description = '';
    function setTitle(e) {
        title = e.target.value;
    }

    let books = [];
    function addBook() {
        const newBook = {
            title : title,
            price : price,
            description : description
        };

        books = books.concat(newBook);
    }
</script>
<style>
    h1 {
        color: purple;
    }

    section {
        margin: auto;
        width: 30rem;
    }

    label, input, textarea { width: 100% }
</style>
<section>
    <div>
        <label for="title">Title</label>
        <input type="text" id="title" value={title} on:input={setTitle} /> 
    </div>
    <div>
        <label for="price">Price</label>
        <input type="number" id="price" bind:value={price} />
    </div>
    <div>
        <label for="description">Description</label>
        <!-- "Reactive values" + "Binding" -->
        <textarea rows="3" id="description" bind:value={description} />      
    </div>

    <!-- "Props (passing info to children)" -->
    <Book bookTitle={title} bookPrice={price} bookDescription={description} />
    <Button on:click={addBook}>ADD Book</Button>
</section>