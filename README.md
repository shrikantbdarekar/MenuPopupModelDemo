# MenuPopupModelDemo


### **Step 1: Open Your .NET 8 Project in VS2022**
1. Open **Visual Studio 2022**.
2. Create a new **ASP.NET Core Web App (Model-View-Controller)** or open your existing .NET 8 project.

---

### **Step 2: Update Bootstrap & jQuery**
#### **Option 1: Using CDN (Recommended for Simplicity)**
Modify the `Views/Shared/_Layout.cshtml` file to include the latest Bootstrap and jQuery.

Replace the existing Bootstrap and jQuery links with:

```html
<head>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css">
    <script src="https://code.jquery.com/jquery-3.6.4.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
</head>
```

#### **Option 2: Using npm (For Advanced Users)**
If you want to install Bootstrap and jQuery locally, use the following commands:

1. Open a terminal in the project root.
2. Run:
   ```sh
   npm install bootstrap@latest jquery@latest
   ```
3. Add the Bootstrap and jQuery references in `wwwroot/lib` and update `_Layout.cshtml` accordingly.

---

### **Step 3: Implement a Dropdown Menu**
Modify `_Layout.cshtml` inside the `<nav>` section to add a dropdown:

```html
<nav class="navbar navbar-expand-lg navbar-dark bg-dark">
    <div class="container-fluid">
        <a class="navbar-brand" href="#">MyApp</a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
            <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
            <ul class="navbar-nav">
                <li class="nav-item"><a class="nav-link" href="#">Home</a></li>
                <li class="nav-item dropdown">
                    <a class="nav-link dropdown-toggle" href="#" id="dropdownMenuButton" role="button" data-bs-toggle="dropdown">
                        Features
                    </a>
                    <ul class="dropdown-menu">
                        <li><a class="dropdown-item" href="#">Feature 1</a></li>
                        <li><a class="dropdown-item" href="#">Feature 2</a></li>
                        <li><a class="dropdown-item" href="#">Feature 3</a></li>
                    </ul>
                </li>
            </ul>
        </div>
    </div>
</nav>
```

---

### **Step 4: Implement a Modal Popup**
In any Razor view (e.g., `Views/Home/Index.cshtml`), add:

```html
<!-- Button to Open Modal -->
<button type="button" class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#myModal">
    Open Modal
</button>

<!-- Modal -->
<div class="modal fade" id="myModal" tabindex="-1" aria-labelledby="myModalLabel" aria-hidden="true">
    <div class="modal-dialog">
        <div class="modal-content">
            <div class="modal-header">
                <h5 class="modal-title" id="myModalLabel">Modal Title</h5>
                <button type="button" class="btn-close" data-bs-dismiss="modal"></button>
            </div>
            <div class="modal-body">
                This is the modal content.
            </div>
            <div class="modal-footer">
                <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Close</button>
            </div>
        </div>
    </div>
</div>
```

---

### **Step 5: Run & Test**
1. Run the project (`Ctrl + F5`).
2. Test:
   - Click the **dropdown menu** to check if it works.
   - Click the **button** to see if the modal popup appears.

