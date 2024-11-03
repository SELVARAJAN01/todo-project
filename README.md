# To-Do List

This project is a simple and interactive to-do list application built using HTML and JavaScript. It allows users to add and delete tasks, helping them manage their daily activities efficiently.

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Getting Started](#getting-started)
- [Usage](#usage)
- [Contact](#contact)

## Introduction
The To-Do List project provides a user-friendly interface to add and remove tasks. This application serves as a basic example of DOM manipulation using JavaScript.

## Features
- Add new tasks to the list.
- Delete tasks from the list.
- Real-time updates of the task list.

## Getting Started
1. Clone the repository from GitHub.
2. Ensure you have an HTML viewer or a web browser to open the `index.html` file.
3. Open `index.html` in your preferred browser to use the to-do list.

## Usage
- **Add Task**: Enter a task in the input field and click the "Add" button to add it to the list.
- **Delete Task**: Click the "Delete" button next to a task to remove it from the list.

## HTML Code
```html
<input id="input">
<button onclick="add()">Add</button>
<ul id="list-container">
    <li>Hello
        <button onclick="deleteItem(event)">Delete</button>
    </li>
</ul>
<script>
    var ul=document.getElementById("list-container")
    var input=document.getElementById("input")
    function add(){
        var listitem=document.createElement("li")
        listitem.innerHTML=input.value+"<button onclick='deleteItem(event)'>Delete</button>"
        ul.append(listitem)
    }
    function deleteItem(event){
        event.target.parentElement.remove()
    }
</script>
