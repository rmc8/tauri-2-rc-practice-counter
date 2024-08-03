<script lang="ts">
    let count: number = 0;

    function increment(): void {
        count++;
    }

    function decrement(): void {
        if (count > 0) {
            count--;
        }
    }

    function reset(): void {
        count = 0;
    }
</script>

<div class="container">
    <h1>Welcome to Counter App powered by Tauri!</h1>

    <div class="counter">
        <p>現在の数値: <span class="count">{count}</span></p>
        <div class="buttons">
            <button on:click={decrement}>-</button>
            <button on:click={reset} class="reset-button">リセット</button>
            <button on:click={increment}>+</button>
        </div>
    </div>
</div>

<style>
    .container {
        text-align: center;
        padding: 2rem;
    }

    h1 {
        color: #2c3e50;
        margin-bottom: 2rem;
    }

    .counter {
        background-color: #f8f9fa;
        border-radius: 8px;
        padding: 2rem;
        box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    }

    .count {
        font-size: 2rem;
        font-weight: bold;
        color: #3498db;
    }

    .buttons {
        margin-top: 1rem;
    }

    button {
        font-size: 1.2rem;
        margin: 0 0.5rem;
        padding: 0.5rem 1rem;
        border: none;
        border-radius: 4px;
        cursor: pointer;
        transition: background-color 0.3s;
    }

    button:nth-child(1) {
        background-color: #e74c3c;
        color: white;
    }

    button:nth-child(2) {
        background-color: #2ecc71;
        color: white;
    }

    button:nth-child(3) {
        background-color: #3498db;
        color: white;
    }

    button:hover {
        opacity: 0.8;
    }
</style>
