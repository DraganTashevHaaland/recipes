<template>
    <header>
        <nav>
            <ul>
                <li><nuxt-link to="/">Starting Page</nuxt-link></li>                                <li><nuxt-link to="/">Starting Page</nuxt-link></li>
                <li><nuxt-link to="/recipes">Recipes</nuxt-link></li>
                <li><nuxt-link to="/about">About</nuxt-link></li>
            </ul>
        </nav>
    </header>
</template>

<style>
header {
    width: 100%;
    height: 30px;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: #531751;
}

ul {
    list-style: none;
    justify-content: center;
    padding: 0;
    margin: 0;
    display: flex;
}

li {
    margin: 0 10px;
}

a {
    text-decoration: none;
    color: white;
}

</style>