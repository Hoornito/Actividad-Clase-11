<template>
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
    <a class="navbar-brand">Entradas mundial 2022</a>
    <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNavDropdown" aria-controls="navbarNavDropdown" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNavDropdown">
        <ul class="navbar-nav">
        <li class="nav-item active">
            <a class="nav-link" href="http://localhost:3000/">Home <span class="sr-only"></span></a>
        </li>
        <li class="nav-item">
            <a class="nav-link" href="Test">Test</a>
        </li>
        <li class="nav-item">
            <a class="nav-link" href="Test 2">Test 2</a>
        </li>
        <li class="dropdown">
            <button class="btn btn-secondary dropdown-toggle" type="button" id="dropdownMenuButton" data-bs-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                Test Menu
            </button>
            <div class="dropdown-menu" aria-labelledby="dropdownMenuButton">
                <a class="dropdown-item" href="Test">Test</a>
                <a class="dropdown-item" href="Test 2">Test 2</a>
                <a class="dropdown-item" href="Hola mundo">Hola mundo</a>
            </div>
        </li>
        <!-- Este no funciona por alguna razon el dropdown. 
            <li class="nav-item dropdown">
            <a class="nav-link dropdown-toggle" id="navbarDropdownMenuLink" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
            Menu
            </a>
            <div class="dropdown-menu" aria-labelledby="navbarDropdownMenuLink">
            <a class="dropdown-item" href="#">Test 1</a>
            <a class="dropdown-item" href="#">Test 2</a>
            <a class="dropdown-item" href="#">Test Settings</a>
            </div>
        </li> -->
        </ul>
    </div>
    </nav>
</template>