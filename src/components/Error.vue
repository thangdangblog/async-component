<template>
    <div class="error-page">
        <h1>Error</h1>
        <p>Oops! Something went wrong.</p>
        <!-- Additional error information or custom error message can be added here -->
    </div>
</template>

<style scoped>
.error-page {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 100vh;
    background-color: rgb(122, 36, 36);
    position: absolute;
    left: 0;
    top: 0;
    width: 100%;
    color: white;
}

.error-page h1 {
    font-size: 24px;
    margin-bottom: 16px;
}

.error-page p {
    font-size: 16px;
}
</style>
