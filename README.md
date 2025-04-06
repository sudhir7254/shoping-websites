<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mee-wesite-Demo</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        :root {
            --primary-color: #f57224;
            --secondary-color: #2874f0;
            --dark-color: #212121;
            --light-color: #f5f5f5;
        }

        body {
            font-family: 'Roboto', sans-serif;
            background-color: #fff;
            color: var(--dark-color);
            transition: all 0.3s ease;
        }

        body.dark-mode {
            background-color: #121212;
            color: #f5f5f5;
        }

        .dark-mode .card,
        .dark-mode .modal-content {
            background-color: #1e1e1e;
            color: #f5f5f5;
            border-color: #333;
        }

        .hero-section {
            margin-top: -20px;
        }

        .product-card {
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .product-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
        }

        .payment-icon {
            height: 30px;
            margin-right: 10px;
        }

        /* Animation classes */
        .fade-in {
            animation: fadeIn 0.5s ease-in;
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        .slide-up {
            animation: slideUp 0.5s ease-out;
        }

        @keyframes slideUp {
            from { transform: translateY(20px); opacity: 0; }
            to { transform: translateY(0); opacity: 1; }
        }

        /* Responsive adjustments */
        @media (max-width: 768px) {
            .hero-section {
                margin-top: 0;
            }
        }
    </style>
</head>
<body>
    <!-- Header/Navbar -->
    <header>
        <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
            <div class="container">
                <a class="navbar-brand" href="#">MEE App</a>
                <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
                    <span class="navbar-toggler-icon"></span>
                </button>
                <div class="collapse navbar-collapse" id="navbarNav">
                    <ul class="navbar-nav me-auto">
                        <li class="nav-item"><a class="nav-link active" href="#">Home</a></li>
                        <li class="nav-item"><a class="nav-link" href="#products">Products</a></li>
                        <li class="nav-item"><a class="nav-link" href="#categories">Categories</a></li>
                        <li class="nav-item"><a class="nav-link" href="#about">About</a></li>
                        <li class="nav-item"><a class="nav-link" href="#contact">Contact</a></li>
                    </ul>
                    <div class="d-flex">
                        <button id="darkModeToggle" class="btn btn-outline-light me-2">
                            <i class="fas fa-moon"></i>
                        </button>
                        <a href="#cart" class="btn btn-outline-light me-2">
                            <i class="fas fa-shopping-cart"></i> Cart <span class="cart-count">0</span>
                        </a>
                        <button class="btn btn-outline-light me-2" data-bs-toggle="modal" data-bs-target="#loginModal">
                            <i class="fas fa-sign-in-alt"></i> Login
                        </button>
                        <button class="btn btn-outline-light" data-bs-toggle="modal" data-bs-target="#registerModal">
                            <i class="fas fa-user-plus"></i> Register
                        </button>
                    </div>
                </div>
            </div>
        </nav>
    </header>

    <main class="container my-4">
        <!-- Hero Section -->
        <div class="hero-section mb-5">
            <div id="carouselExample" class="carousel slide" data-bs-ride="carousel">
                <div class="carousel-inner">
                    <div class="carousel-item active">
                        <img src="https://images.unsplash.com/photo-1607082348824-0a96f2a4b9da?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" class="d-block w-100" alt="Banner 1">
                    </div>
                    <div class="carousel-item">
                        <img src="https://images.unsplash.com/photo-1523275335684-37898b6baf30?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" class="d-block w-100" alt="Banner 2">
                    </div>
                    <div class="carousel-item">
                        <img src="https://images.unsplash.com/photo-1505740420928-5e560c06d30e?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" class="d-block w-100" alt="Banner 3">
                    </div>
                </div>
                <button class="carousel-control-prev" type="button" data-bs-target="#carouselExample" data-bs-slide="prev">
                    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
                    <span class="visually-hidden">Previous</span>
                </button>
                <button class="carousel-control-next" type="button" data-bs-target="#carouselExample" data-bs-slide="next">
                    <span class="carousel-control-next-icon" aria-hidden="true"></span>
                    <span class="visually-hidden">Next</span>
                </button>
            </div>
        </div>

        <!-- Featured Products -->
        <section id="products" class="mb-5">
            <h2 class="text-center mb-4">Featured Products</h2>
            <div class="row">
                <div class="col-md-3 mb-4">
                    <div class="card h-100 product-card">
                        <img src="https://images.unsplash.com/photo-1546868871-7041f2a55e12?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" class="card-img-top" alt="Smart Watch">
                        <div class="card-body">
                            <h5 class="card-title">Smart Watch</h5>
                            <p class="card-text">Rs. 5,999.00</p>
                            <div class="d-flex justify-content-between">
                                <button class="btn btn-sm btn-outline-primary view-product" data-id="1">View</button>
                                <button class="btn btn-sm btn-primary add-to-cart" data-id="1">Add to Cart</button>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col-md-3 mb-4">
                    <div class="card h-100 product-card">
                        <img src="https://images.unsplash.com/photo-1505740420928-5e560c06d30e?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" class="card-img-top" alt="Headphones">
                        <div class="card-body">
                            <h5 class="card-title">Wireless Headphones</h5>
                            <p class="card-text">Rs. 3,499.00</p>
                            <div class="d-flex justify-content-between">
                                <button class="btn btn-sm btn-outline-primary view-product" data-id="2">View</button>
                                <button class="btn btn-sm btn-primary add-to-cart" data-id="2">Add to Cart</button>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col-md-3 mb-4">
                    <div class="card h-100 product-card">
                        <img src="https://images.unsplash.com/photo-1523275335684-37898b6baf30?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" class="card-img-top" alt="Smartphone">
                        <div class="card-body">
                            <h5 class="card-title">Smartphone X</h5>
                            <p class="card-text">Rs. 32,999.00</p>
                            <div class="d-flex justify-content-between">
                                <button class="btn btn-sm btn-outline-primary view-product" data-id="3">View</button>
                                <button class="btn btn-sm btn-primary add-to-cart" data-id="3">Add to Cart</button>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col-md-3 mb-4">
                    <div class="card h-100 product-card">
                        <img src="https://images.unsplash.com/photo-1542291026-7eec264c27ff?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" class="card-img-top" alt="Running Shoes">
                        <div class="card-body">
                            <h5 class="card-title">Running Shoes</h5>
                            <p class="card-text">Rs. 4,599.00</p>
                            <div class="d-flex justify-content-between">
                                <button class="btn btn-sm btn-outline-primary view-product" data-id="4">View</button>
                                <button class="btn btn-sm btn-primary add-to-cart" data-id="4">Add to Cart</button>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Categories -->
        <section id="categories" class="mb-5">
            <h2 class="text-center mb-4">Categories</h2>
            <div class="row">
                <div class="col-md-2 mb-3 text-center">
                    <div class="category-card p-3 border rounded">
                        <img src="https://images.unsplash.com/photo-1526170375885-4d8ecf77b99f?ixlib=rb-1.2.1&auto=format&fit=crop&w=100&q=80" class="img-fluid rounded-circle mb-2" width="80" height="80">
                        <h6>Electronics</h6>
                    </div>
                </div>
                <div class="col-md-2 mb-3 text-center">
                    <div class="category-card p-3 border rounded">
                        <img src="https://images.unsplash.com/photo-1526170375885-4d8ecf77b99f?ixlib=rb-1.2.1&auto=format&fit=crop&w=100&q=80" class="img-fluid rounded-circle mb-2" width="80" height="80">
                        <h6>Clothing</h6>
                    </div>
                </div>
                <div class="col-md-2 mb-3 text-center">
                    <div class="category-card p-3 border rounded">
                        <img src="https://images.unsplash.com/photo-1526170375885-4d8ecf77b99f?ixlib=rb-1.2.1&auto=format&fit=crop&w=100&q=80" class="img-fluid rounded-circle mb-2" width="80" height="80">
                        <h6>Home & Kitchen</h6>
                    </div>
                </div>
                <div class="col-md-2 mb-3 text-center">
                    <div class="category-card p-3 border rounded">
                        <img src="https://images.unsplash.com/photo-1526170375885-4d8ecf77b99f?ixlib=rb-1.2.1&auto=format&fit=crop&w=100&q=80" class="img-fluid rounded-circle mb-2" width="80" height="80">
                        <h6>Beauty</h6>
                    </div>
                </div>
                <div class="col-md-2 mb-3 text-center">
                    <div class="category-card p-3 border rounded">
                        <img src="https://images.unsplash.com/photo-1526170375885-4d8ecf77b99f?ixlib=rb-1.2.1&auto=format&fit=crop&w=100&q=80" class="img-fluid rounded-circle mb-2" width="80" height="80">
                        <h6>Toys</h6>
                    </div>
                </div>
                <div class="col-md-2 mb-3 text-center">
                    <div class="category-card p-3 border rounded">
                        <img src="https://images.unsplash.com/photo-1526170375885-4d8ecf77b99f?ixlib=rb-1.2.1&auto=format&fit=crop&w=100&q=80" class="img-fluid rounded-circle mb-2" width="80" height="80">
                        <h6>Sports</h6>
                    </div>
                </div>
            </div>
        </section>

        <!-- About Section -->
        <section id="about" class="mb-5">
            <div class="card">
                <div class="card-body">
                    <h2 class="card-title">About MEE App</h2>
                    <p class="card-text">Welcome to MEE App, your one-stop destination for all your shopping needs. We offer a wide range of products at competitive prices.</p>
                    <p>Developed by Sudhir Yadav</p>
                    <p>Email: iamsudhir72544@gmail.com</p>
                    <p>Location: Janakpur</p>
                </div>
            </div>
        </section>

        <!-- Contact Section -->
        <section id="contact" class="mb-5">
            <div class="card">
                <div class="card-body">
                    <h2 class="card-title">Contact Us</h2>
                    <form id="contactForm">
                        <div class="mb-3">
                            <label for="name" class="form-label">Name</label>
                            <input type="text" class="form-control" id="name" required>
                        </div>
                        <div class="mb-3">
                            <label for="email" class="form-label">Email</label>
                            <input type="email" class="form-control" id="email" required>
                        </div>
                        <div class="mb-3">
                            <label for="message" class="form-label">Message</label>
                            <textarea class="form-control" id="message" rows="3" required></textarea>
                        </div>
                        <button type="submit" class="btn btn-primary">Submit</button>
                    </form>
                </div>
            </div>
        </section>

        <!-- Product Detail Modal -->
        <div class="modal fade" id="productModal" tabindex="-1" aria-hidden="true">
            <div class="modal-dialog modal-lg">
                <div class="modal-content">
                    <div class="modal-header">
                        <h5 class="modal-title" id="productModalTitle">Product Details</h5>
                        <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                    </div>
                    <div class="modal-body">
                        <div class="row">
                            <div class="col-md-6">
                                <img src="" class="img-fluid" id="productModalImage" alt="Product Image">
                            </div>
                            <div class="col-md-6">
                                <h3 id="productModalName"></h3>
                                <h4 class="my-3" id="productModalPrice"></h4>
                                <p id="productModalDescription"></p>
                                <div class="d-flex align-items-center mb-3">
                                    <button class="btn btn-outline-secondary minus-btn">-</button>
                                    <input type="number" class="form-control text-center mx-2 quantity-input" value="1" min="1" style="width: 60px;">
                                    <button class="btn btn-outline-secondary plus-btn">+</button>
                                </div>
                                <button class="btn btn-primary w-100 add-to-cart-modal">Add to Cart</button>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Login Modal -->
        <div class="modal fade" id="loginModal" tabindex="-1" aria-hidden="true">
            <div class="modal-dialog">
                <div class="modal-content">
                    <div class="modal-header">
                        <h5 class="modal-title">Login</h5>
                        <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                    </div>
                    <div class="modal-body">
                        <form id="loginForm">
                            <div class="mb-3">
                                <label for="loginEmail" class="form-label">Email</label>
                                <input type="email" class="form-control" id="loginEmail" required>
                            </div>
                            <div class="mb-3">
                                <label for="loginPassword" class="form-label">Password</label>
                                <input type="password" class="form-control" id="loginPassword" required>
                            </div>
                            <button type="submit" class="btn btn-primary w-100">Login</button>
                        </form>
                        <div class="text-center mt-3">
                            <p>Don't have an account? <a href="#" data-bs-toggle="modal" data-bs-target="#registerModal" data-bs-dismiss="modal">Register here</a></p>
                        </div>
                        <div id="loginMessage" class="mt-3"></div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Register Modal -->
        <div class="modal fade" id="registerModal" tabindex="-1" aria-hidden="true">
            <div class="modal-dialog">
                <div class="modal-content">
                    <div class="modal-header">
                        <h5 class="modal-title">Register</h5>
                        <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                    </div>
                    <div class="modal-body">
                        <form id="registerForm">
                            <div class="mb-3">
                                <label for="registerName" class="form-label">Full Name</label>
                                <input type="text" class="form-control" id="registerName" required>
                            </div>
                            <div class="mb-3">
                                <label for="registerEmail" class="form-label">Email</label>
                                <input type="email" class="form-control" id="registerEmail" required>
                            </div>
                            <div class="mb-3">
                                <label for="registerPhone" class="form-label">Phone Number</label>
                                <input type="tel" class="form-control" id="registerPhone" required>
                            </div>
                            <div class="mb-3">
                                <label for="registerPassword" class="form-label">Password</label>
                                <input type="password" class="form-control" id="registerPassword" required>
                            </div>
                            <div class="mb-3">
                                <label for="registerConfirmPassword" class="form-label">Confirm Password</label>
                                <input type="password" class="form-control" id="registerConfirmPassword" required>
                            </div>
                            <button type="submit" class="btn btn-primary w-100">Register</button>
                        </form>
                        <div class="text-center mt-3">
                            <p>Already have an account? <a href="#" data-bs-toggle="modal" data-bs-target="#loginModal" data-bs-dismiss="modal">Login here</a></p>
                        </div>
                        <div id="registerMessage" class="mt-3"></div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Cart Modal -->
        <div class="modal fade" id="cartModal" tabindex="-1" aria-hidden="true">
            <div class="modal-dialog modal-lg">
                <div class="modal-content">
                    <div class="modal-header">
                        <h5 class="modal-title">Your Cart</h5>
                        <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                    </div>
                    <div class="modal-body">
                        <div class="table-responsive">
                            <table class="table">
                                <thead>
                                    <tr>
                                        <th>Product</th>
                                        <th>Price</th>
                                        <th>Quantity</th>
                                        <th>Total</th>
                                        <th>Action</th>
                                    </tr>
                                </thead>
                                <tbody id="cartItems">
                                    <!-- Cart items will be added here -->
                                </tbody>
                            </table>
                        </div>
                        <div class="text-end">
                            <h5>Total: Rs. <span id="cartTotal">0.00</span></h5>
                        </div>
                    </div>
                    <div class="modal-footer">
                        <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Continue Shopping</button>
                        <button type="button" class="btn btn-primary" id="checkoutBtn">Proceed to Checkout</button>
                    </div>
                </div>
            </div>
        </div>

        <!-- Checkout Modal -->
        <div class="modal fade" id="checkoutModal" tabindex="-1" aria-hidden="true">
            <div class="modal-dialog modal-lg">
                <div class="modal-content">
                    <div class="modal-header">
                        <h5 class="modal-title">Checkout</h5>
                        <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                    </div>
                    <div class="modal-body">
                        <div class="row">
                            <div class="col-md-6">
                                <h5>Shipping Information</h5>
                                <form id="shippingForm">
                                    <div class="mb-3">
                                        <label for="fullName" class="form-label">Full Name</label>
                                        <input type="text" class="form-control" id="fullName" required>
                                    </div>
                                    <div class="mb-3">
                                        <label for="address" class="form-label">Address</label>
                                        <textarea class="form-control" id="address" rows="3" required></textarea>
                                    </div>
                                    <div class="mb-3">
                                        <label for="city" class="form-label">City</label>
                                        <input type="text" class="form-control" id="city" required>
                                    </div>
                                    <div class="mb-3">
                                        <label for="phone" class="form-label">Phone</label>
                                        <input type="tel" class="form-control" id="phone" required>
                                    </div>
                                </form>
                            </div>
                            <div class="col-md-6">
                                <h5>Order Summary</h5>
                                <div class="card">
                                    <div class="card-body">
                                        <div id="checkoutItems">
                                            <!-- Order items will be added here -->
                                        </div>
                                        <hr>
                                        <div class="d-flex justify-content-between">
                                            <h6>Subtotal:</h6>
                                            <h6>Rs. <span id="checkoutSubtotal">0.00</span></h6>
                                        </div>
                                        <div class="d-flex justify-content-between">
                                            <h6>Shipping:</h6>
                                            <h6>Rs. 100.00</h6>
                                        </div>
                                        <hr>
                                        <div class="d-flex justify-content-between">
                                            <h5>Total:</h5>
                                            <h5>Rs. <span id="checkoutTotal">0.00</span></h5>
                                        </div>
                                    </div>
                                </div>

                                <h5 class="mt-3">Payment Method</h5>
                                <div class="form-check mb-2">
                                    <input class="form-check-input" type="radio" name="paymentMethod" id="cod" value="cod" checked>
                                    <label class="form-check-label" for="cod">
                                        Cash on Delivery
                                    </label>
                                </div>
                                <div class="form-check mb-2">
                                    <input class="form-check-input" type="radio" name="paymentMethod" id="esewa" value="esewa">
                                    <label class="form-check-label" for="esewa">
                                        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/7d/Esewa_logo.svg/1200px-Esewa_logo.svg.png" alt="eSewa" style="height: 20px;">
                                    </label>
                                </div>
                                <div class="form-check mb-2">
                                    <input class="form-check-input" type="radio" name="paymentMethod" id="khalti" value="khalti">
                                    <label class="form-check-label" for="khalti">
                                        <img src="https://khalti.com/static/img/logo.png" alt="Khalti" style="height: 20px;">
                                    </label>
                                </div>
                                <div class="form-check">
                                    <input class="form-check-input" type="radio" name="paymentMethod" id="imepay" value="imepay">
                                    <label class="form-check-label" for="imepay">
                                        <img src="https://www.imemobile.com/wp-content/uploads/2019/12/ime-logo.png" alt="IME Pay" style="height: 20px;">
                                    </label>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="modal-footer">
                        <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Cancel</button>
                        <button type="button" class="btn btn-primary" id="placeOrderBtn">Place Order</button>
                    </div>
                </div>
            </div>
        </div>

        <!-- Order Success Modal -->
        <div class="modal fade" id="orderSuccessModal" tabindex="-1" aria-hidden="true">
            <div class="modal-dialog">
                <div class="modal-content">
                    <div class="modal-header">
                        <h5 class="modal-title">Order Placed Successfully!</h5>
                        <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                    </div>
                    <div class="modal-body text-center">
                        <i class="fas fa-check-circle text-success mb-3" style="font-size: 5rem;"></i>
                        <h4>Thank you for your order!</h4>
                        <p>Your order has been placed successfully. We will contact you soon.</p>
                        <p>Order ID: <strong>ORD-<span id="orderId">12345</span></strong></p>
                    </div>
                    <div class="modal-footer justify-content-center">
                        <button type="button" class="btn btn-primary" data-bs-dismiss="modal">Continue Shopping</button>
                    </div>
                </div>
            </div>
        </div>
    </main>

    <!-- Footer -->
    <footer class="bg-dark text-white py-4">
        <div class="container">
            <div class="row">
                <div class="col-md-4">
                    <h5>About MEE App</h5>
                    <p>Developed by Sudhir Yadav</p>
                    <p>Email: iamsudhir72544@gmail.com</p>
                    <p>Location: Janakpur</p>
                </div>
                <div class="col-md-4">
                    <h5>Quick Links</h5>
                    <ul class="list-unstyled">
                        <li><a href="#" class="text-white">Home</a></li>
                        <li><a href="#products" class="text-white">Products</a></li>
                        <li><a href="#contact" class="text-white">Contact Us</a></li>
                        <li><a href="#" class="text-white">Privacy Policy</a></li>
                    </ul>
                </div>
                <div class="col-md-4">
                    <h5>Payment Methods</h5>
                    <div class="payment-methods">
                        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/7d/Esewa_logo.svg/1200px-Esewa_logo.svg.png" alt="eSewa" class="payment-icon">
                        <img src="https://khalti.com/static/img/logo.png" alt="Khalti" class="payment-icon">
                        <img src="https://www.imemobile.com/wp-content/uploads/2019/12/ime-logo.png" alt="IME Pay" class="payment-icon">
                        <img src="https://logos-download.com/wp-content/uploads/2021/01/PhonePe_Logo.png" alt="PhonePe" class="payment-icon">
                    </div>
                </div>
            </div>
            <div class="text-center mt-3">
                <p>&copy; 2023 MEE App. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
    <script>
    $(document).ready(function() {
        // Sample product data
        const products = [
            {
                id: 1,
                name: "Smart Watch",
                price: 5999.00,
                image: "https://images.unsplash.com/photo-1546868871-7041f2a55e12?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80",
                description: "Feature-rich smart watch with health monitoring and notifications."
            },
            {
                id: 2,
                name: "Wireless Headphones",
                price: 3499.00,
                image: "https://images.unsplash.com/photo-1505740420928-5e560c06d30e?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80",
                description: "High-quality wireless headphones with noise cancellation."
            },
            {
                id: 3,
                name: "Smartphone X",
                price: 32999.00,
                image: "https://images.unsplash.com/photo-1523275335684-37898b6baf30?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80",
                description: "Latest smartphone with advanced camera and processor."
            },

            {
                id: 4,
                name: "Smartphone X",
                price: 32999.00,
                image: "https://images.unsplash.com/photo-1511707171634-5f897ff02aa9?q=80&w=2080&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D",
                description: "Latest smartphone with advanced camera and processor."
            },

            {
                id: 4,
                name: "Clothes",
                price: 32999.00,
                image: "https://images.unsplash.com/photo-1489987707025-afc232f7ea0f?q=80&w=2070&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D",
                description: "stylish clothes"
            },

            {
                id: 4,
                name: "Smartphone X",
                price: 32999.00,
                image: "https://images.unsplash.com/photo-1511707171634-5f897ff02aa9?q=80&w=2080&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D",
                description: "Latest smartphone with advanced camera and processor."
            },
            {
                id: 5,
                name: "Running Shoes",
                price: 4599.00,
                image: "https://images.unsplash.com/photo-1542291026-7eec264c27ff?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80",
                description: "Comfortable running shoes with excellent cushioning."
            }
        ];

        // Cart functionality
        let cart = JSON.parse(localStorage.getItem('cart')) || [];

        // Dark mode toggle
        $('#darkModeToggle').click(function() {
            $('body').toggleClass('dark-mode');
            if($('body').hasClass('dark-mode')) {
                $(this).html('<i class="fas fa-sun"></i>');
            } else {
                $(this).html('<i class="fas fa-moon"></i>');
            }
        });

        // View product details
        $('.view-product').click(function() {
            const productId = $(this).data('id');
            const product = products.find(p => p.id == productId);
            
            $('#productModalTitle').text(product.name);
            $('#productModalName').text(product.name);
            $('#productModalPrice').text('Rs. ' + product.price.toFixed(2));
            $('#productModalDescription').text(product.description);
            $('#productModalImage').attr('src', product.image);
            $('#productModal').modal('show');
        });

        // Add to cart from product listing
        $('.add-to-cart').click(function() {
            const productId = $(this).data('id');
            const product = products.find(p => p.id == productId);
            
            addToCart(product, 1);
            showNotification(`${product.name} added to cart`);
        });

        // Add to cart from product modal
        $(document).on('click', '.add-to-cart-modal', function() {
            const productId = $('.view-product').data('id');
            const product = products.find(p => p.id == productId);
            const quantity = parseInt($('.quantity-input').val());
            
            addToCart(product, quantity);
            showNotification(`${quantity} ${product.name}(s) added to cart`);
            $('#productModal').modal('hide');
        });

        // Quantity buttons
        $(document).on('click', '.plus-btn', function() {
            const input = $(this).siblings('.quantity-input');
            input.val(parseInt(input.val()) + 1);
        });

        $(document).on('click', '.minus-btn', function() {
            const input = $(this).siblings('.quantity-input');
            const value = parseInt(input.val());
            if(value > 1) {
                input.val(value - 1);
            }
        });

        // Show cart
        $('a[href="#cart"]').click(function(e) {
            e.preventDefault();
            updateCartDisplay();
            $('#cartModal').modal('show');
        });

        // Checkout button
        $('#checkoutBtn').click(function() {
            $('#cartModal').modal('hide');
            updateCheckoutDisplay();
            $('#checkoutModal').modal('show');
        });

        // Place order
        $('#placeOrderBtn').click(function() {
            // In a real app, this would send data to server
            const orderId = 'ORD-' + Math.floor(10000 + Math.random() * 90000);
            $('#orderId').text(orderId);
            
            // Clear cart
            cart = [];
            localStorage.setItem('cart', JSON.stringify(cart));
            updateCartCount();
            
            $('#checkoutModal').modal('hide');
            $('#orderSuccessModal').modal('show');
        });

        // Login form
        $('#loginForm').submit(function(e) {
            e.preventDefault();
            $('#loginMessage').html('<div class="alert alert-success">Login successful (demo)</div>');
            setTimeout(() => {
                $('#loginModal').modal('hide');
            }, 1500);
        });

        // Register form
        $('#registerForm').submit(function(e) {
            e.preventDefault();
            if($('#registerPassword').val() !== $('#registerConfirmPassword').val()) {
                $('#registerMessage').html('<div class="alert alert-danger">Passwords do not match</div>');
                return;
            }
            $('#registerMessage').html('<div class="alert alert-success">Registration successful (demo)</div>');
            setTimeout(() => {
                $('#registerModal').modal('hide');
            }, 1500);
        });

        // Contact form
        $('#contactForm').submit(function(e) {
            e.preventDefault();
            alert('Thank you for your message! (This is a demo)');
            $('#contactForm')[0].reset();
        });

        // Helper function to add to cart
        function addToCart(product, quantity) {
            const existingItem = cart.find(item => item.id === product.id);
            
            if(existingItem) {
                existingItem.quantity += quantity;
            } else {
                cart.push({
                    id: product.id,
                    name: product.name,
                    price: product.price,
                    image: product.image,
                    quantity: quantity
                });
            }
            
            localStorage.setItem('cart', JSON.stringify(cart));
            updateCartCount();
        }

        // Helper function to update cart display
        function updateCartDisplay() {
            const cartItems = $('#cartItems');
            cartItems.empty();
            
            let total = 0;
            
            cart.forEach(item => {
                const itemTotal = item.price * item.quantity;
                total += itemTotal;
                
                cartItems.append(`
                    <tr>
                        <td>
                            <div class="d-flex align-items-center">
                                <img src="${item.image}" width="50" height="50" class="me-3">
                                ${item.name}
                            </div>
                        </td>
                        <td>Rs. ${item.price.toFixed(2)}</td>
                        <td>
                            <div class="d-flex align-items-center">
                                <button class="btn btn-sm btn-outline-secondary minus-cart" data-id="${item.id}">-</button>
                                <input type="number" class="form-control text-center mx-2 cart-quantity" value="${item.quantity}" min="1" style="width: 60px;" data-id="${item.id}">
                                <button class="btn btn-sm btn-outline-secondary plus-cart" data-id="${item.id}">+</button>
                            </div>
                        </td>
                        <td>Rs. ${itemTotal.toFixed(2)}</td>
                        <td><button class="btn btn-sm btn-danger remove-cart" data-id="${item.id}"><i class="fas fa-trash"></i></button></td>
                    </tr>
                `);
            });
            
            $('#cartTotal').text(total.toFixed(2));
        }

        // Helper function to update checkout display
        function updateCheckoutDisplay() {
            const checkoutItems = $('#checkoutItems');
            checkoutItems.empty();
            
            let subtotal = 0;
            
            cart.forEach(item => {
                const itemTotal = item.price * item.quantity;
                subtotal += itemTotal;
                
                checkoutItems.append(`
                    <div class="d-flex justify-content-between mb-2">
                        <span>${item.name} x ${item.quantity}</span>
                        <span>Rs. ${itemTotal.toFixed(2)}</span>
                    </div>
                `);
            });
            
            $('#checkoutSubtotal').text(subtotal.toFixed(2));
            $('#checkoutTotal').text((subtotal + 100).toFixed(2));
        }

        // Helper function to update cart count
        function updateCartCount() {
            const count = cart.reduce((total, item) => total + item.quantity, 0);
            $('.cart-count').text(count);
        }

        // Helper function to show notification
        function showNotification(message) {
            const notification = $(`
                <div class="position-fixed bottom-0 end-0 p-3" style="z-index: 11">
                    <div class="toast show" role="alert" aria-live="assertive" aria-atomic="true">
                        <div class="toast-header">
                            <strong class="me-auto">Cart Updated</strong>
                            <button type="button" class="btn-close" data-bs-dismiss="toast" aria-label="Close"></button>
                        </div>
                        <div class="toast-body">
                            ${message}
                        </div>
                    </div>
                </div>
            `);
            
            $('body').append(notification);
            setTimeout(() => notification.remove(), 3000);
        }

        // Cart quantity controls
        $(document).on('click', '.plus-cart', function() {
            const productId = $(this).data('id');
            const item = cart.find(item => item.id == productId);
            item.quantity++;
            localStorage.setItem('cart', JSON.stringify(cart));
            updateCartDisplay();
            updateCartCount();
        });

        $(document).on('click', '.minus-cart', function() {
            const productId = $(this).data('id');
            const item = cart.find(item => item.id == productId);
            if(item.quantity > 1) {
                item.quantity--;
                localStorage.setItem('cart', JSON.stringify(cart));
                updateCartDisplay();
                updateCartCount();
            }
        });

        $(document).on('change', '.cart-quantity', function() {
            const productId = $(this).data('id');
            const quantity = parseInt($(this).val());
            const item = cart.find(item => item.id == productId);
            
            if(quantity >= 1) {
                item.quantity = quantity;
                localStorage.setItem('cart', JSON.stringify(cart));
                updateCartDisplay();
                updateCartCount();
            }
        });

        $(document).on('click', '.remove-cart', function() {
            const productId = $(this).data('id');
            cart = cart.filter(item => item.id != productId);
            localStorage.setItem('cart', JSON.stringify(cart));
            updateCartDisplay();
            updateCartCount();
            showNotification('Item removed from cart');
        });

        // Initialize cart count
        updateCartCount();
    });
    </script>
</body>
</html>
