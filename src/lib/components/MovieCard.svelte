<div class="container">
    <div class="card">
        <!-- svelte-ignore a11y_img_redundant_alt -->
        <img src="https://via.placeholder.com/150" alt="Card Image" class="card-image" />
        <div class="card-content">
            <h2 class="card-title">Card Title</h2>
            <p class="card-description">This is a brief description of the content inside the card. It is concise and to the point.</p>
            <button class="card-button">Learn More</button>
        </div>
    </div>
    
</div>

<style>
      /* General card styling */
.card {
    width: 300px;
    border: 1px solid #e0e0e0;
    border-radius: 10px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    overflow: hidden;
    transition: transform 0.3s, box-shadow 0.3s;
    background: #fff;
}

/* Image styling */
.card-image {
    width: 100%;
    height: 150px;
    object-fit: cover;
}

/* Content styling */
.card-content {
    padding: 15px;
    text-align: center;
}

.card-title {
    font-size: 1.5rem;
    color: #333;
    margin: 10px 0;
}

.card-description {
    font-size: 0.9rem;
    color: #555;
    margin: 10px 0 20px;
    line-height: 1.5;
}

/* Button styling */
.card-button {
    display: inline-block;
    padding: 10px 20px;
    font-size: 1rem;
    color: #fff;
    background-color: orangered;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    transition: background-color 0.3s;
}

.card-button:hover {
    background-color: #d73716;
}

/* Hover effect for card */
.card:hover {
    transform: translateY(-10px);
    box-shadow: 0 8px 12px rgba(0, 0, 0, 0.2);
}

</style>