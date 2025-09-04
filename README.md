<!DOCTYPE html>
<html lang="en">
<head>
    <title>LuxeMart - Premium Shopping Experience</title>
    <link rel="stylesheet" href="style.css">
    <style>
        :root {
            --primary: #2c3e50;
            --secondary: #e74c3c;
            --light: #ecf0f1;
            --dark: #2c3e50;
            --white: #ffffff;
            --text: #333333;
        }
        
* {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  }
        
body {
            background-color: var(--light);
            color: var(--text);
            line-height: 1.6;
     }
        
.container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
header {
            background-color: var(--white);
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
        }
        
nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 0;
        }
        
.logo {
            font-size: 24px;
            font-weight: 700;
            color: var(--primary);
            text-decoration: none;
            display: flex;
            align-items: center;
        }
        
.logo i {
            margin-right: 10px;
            color: var(--secondary);
        }
        
.nav-links {
            display: flex;
            list-style: none;
        }
        
.nav-links li {
            margin-left: 30px;
        }
        
.nav-links a {
            text-decoration: none;
            color: var(--dark);
            font-weight: 500;
            transition: color 0.3s;
        }
        
.nav-links a:hover {
            color: var(--secondary);
        }
        
.cart-icon {
            position: relative;
        }
        
.cart-count {
            position: absolute;
            top: -8px;
            right: -8px;
            background-color: var(--secondary);
            color: var(--white);
            border-radius: 50%;
            width: 20px;
            height: 20px;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 12px;
        }

.hero {
            height: 600px;
            background-image: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url("https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/e5aab477-f8f3-45ad-883a-00485ce50288.png");
            background-size: cover;
            background-position: center;
            display: flex;
            align-items: center;
            text-align: center;
            color: var(--white);
            margin-top: 70px;
            position: relative;
        }
        
.hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.4);
        }
        
.hero-content {
            position: relative;
            z-index: 1;
            max-width: 800px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
.hero h1 {
            font-size: 48px;
            margin-bottom: 20px;
            text-transform: uppercase;
            letter-spacing: 2px;
        }
        
.hero p {
            font-size: 20px;
            margin-bottom: 30px;
        }
        
.btn {
            display: inline-block;
            background-color: var(--secondary);
            color: var(--white);
            padding: 12px 30px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s;
            border: none;
            cursor: pointer;
            text-transform: uppercase;
            letter-spacing: 1px;
        }
        
.btn:hover {
            background-color: var(--primary);
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
        }
        
.section-title {
            text-align: center;
            margin: 60px 0 40px;
            font-size: 36px;
            color: var(--primary);
            position: relative;
        }
        
.section-title::after {
            content: '';
            display: block;
            width: 80px;
            height: 4px;
            background-color: var(--secondary);
            margin: 15px auto 0;
        }
        
.products {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 30px;
            padding: 20px;
        }
        
.product-card {
            background-color: var(--white);
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s, box-shadow 0.3s;
        }
        
.product-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.2);
        }
        
.product-img {
            width: 100%;
            height: 280px;
            object-fit: cover;
        }
        
.product-info {
            padding: 20px;
        }
        
.product-title {
            font-size: 18px;
            margin-bottom: 10px;
            font-weight: 600;
        }
        
.product-desc {
            color: #666;
            margin-bottom: 15px;
            font-size: 14px;
        }
        
.product-price {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
.price {
            font-size: 20px;
            font-weight: 700;
            color: var(--secondary);
        }
        
.add-to-cart {
            background-color: var(--primary);
            color: var(--white);
            border: none;
            padding: 8px 15px;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s;
        }

.add-to-cart:hover {
            background-color: var(--secondary);
        }
        
 
footer {
            background-color: var(--dark);
            color: var(--white);
            padding: 50px 0 20px;
            margin-top: 60px;
        }
        
.footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }
        
.footer-col h3 {
            font-size: 18px;
            margin-bottom: 20px;
            position: relative;
            padding-bottom: 10px;
        }
        
.footer-col h3::after {
            content: '';
            position: absolute;
            left: 0;
            bottom: 0;
            width: 40px;
            height: 2px;
            background-color: var(--secondary);
        }
        
.footer-col p, .footer-col a {
            color: #bbb;
            margin-bottom: 10px;
            display: block;
            text-decoration: none;
            transition: color 0.3s;
        }
        
.footer-col a:hover {
            color: var(--secondary);
        }
        
.social-links {
            display: flex;
            gap: 15px;
        }
        
.social-links a {
            color: var(--white);
            background-color: rgba(255, 255, 255, 0.1);
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: all 0.3s;
        }
        
.social-links a:hover {
            background-color: var(--secondary);
            transform: translateY(-3px);
        }
        
.copyright {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: #bbb;
            font-size: 14px;
        }
        
 .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.7);
            z-index: 2000;
            overflow-y: auto;
        }
        
.modal-content {
            background-color: var(--white);
            width: 90%;
            max-width: 800px;
            margin: 50px auto;
            border-radius: 10px;
            overflow: hidden;
            animation: modalOpen 0.4s;
        }
        
@keyframes modalOpen {
    from {
                opacity: 0;
                transform: translateY(-50px);
         }
    to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
.modal-header {
            background-color: var(--primary);
            color: var(--white);
            padding: 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
.close-modal {
            background: none;
            border: none;
            color: var(--white);
            font-size: 24px;
            cursor: pointer;
        }
        
.cart-items {
            max-height: 400px;
            overflow-y: auto;
            padding: 20px;
        }
        
.cart-item {
            display: flex;
            align-items: center;
            border-bottom: 1px solid #eee;
            padding: 15px 0;
        }
        
.cart-item-img {
            width: 80px;
            height: 80px;
            object-fit: cover;
            border-radius: 5px;
            margin-right: 20px;
        }
        
.cart-item-details {
            flex: 1;
        }
        
.cart-item-title {
            font-weight: 600;
            margin-bottom: 5px;
        }
        
.cart-item-price {
            color: var(--secondary);
            font-weight: 700;
        }
        
.cart-item-quantity {
            display: flex;
            align-items: center;
            margin-top: 10px;
        }
        
.quantity-btn {
            background-color: #f0f0f0;
            border: none;
            width: 25px;
            height: 25px;
            border-radius: 3px;
            cursor: pointer;
            font-size: 16px;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
.quantity {
            margin: 0 10px;
            min-width: 20px;
            text-align: center;
        }
        
.remove-item {
            background: none;
            border: none;
            color: #ff5555;
            cursor: pointer;
            margin-left: 20px;
        }
        
.cart-summary {
            padding: 20px;
            border-top: 1px solid #eee;
        }
        
.total {
            display: flex;
            justify-content: space-between;
            font-size: 18px;
            font-weight: 700;
            margin-bottom: 20px;
        }
        
.checkout-btn {
            width: 100%;
            padding: 15px;
        }
        
       
@media (max-width: 992px) {
    .hero h1 {
                font-size: 36px;
            }
            
    .hero p {
                font-size: 18px;
            }
 }
        
@media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            
            .hero {
                height: 500px;
            }
            
            .hero h1 {
                font-size: 32px;
            }
            
            .hero p {
                font-size: 16px;
            }
}
        
@media (max-width: 576px) {
            .products {
                grid-template-columns: 1fr;
            }
            
            .footer-content {
                grid-template-columns: 1fr;
            }
            
            .hero {
                height: 400px;
            }
            
            .hero h1 {
                font-size: 28px;
            }
}
    </style>
</head>
<body>
    <header>
        <div class="container">
            <nav>
                <a href="#" class="logo">
                    <i class="fas fa-gem"></i> Shopping Mart
                </a>
                <ul class="nav-links">
                    <li><a href="#">Home</a></li>
                    <li><a href="#">Shop</a></li>
                    <li><a href="#">About</a></li>
                    <li><a href="#">Contact</a></li>
                    <li>
                        <a href="#" class="cart-icon" id="cart-icon">
                            <i class="fas fa-shopping-cart"></i>
                            <span class="cart-count">0</span>
                        </a>
                    </li>
                </ul>
            </nav>
        </div>
    </header>

    <section class="hero" id="hero">
        <div class="hero-content">
            <h1>Discover Premium Products</h1>
            <p>Experience luxury shopping with our exclusive collection of handpicked items from around the world.</p>
            <a href="#" class="btn">Shop Now</a>
        </div>
    </section>

    <section class="container">
        <h2 class="section-title">Featured Products</h2>
        <div class="products" id="products">
        </div>
    </section>

    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-col">
                    <h3>About Us</h3>
                    <p>Shopping Mart brings you premium products with exceptional quality and style from around the world.</p>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-pinterest"></i></a>
                    </div>
                </div>
                <div class="footer-col">
                    <h3>Quick Links</h3>
                    <a href="#">Home</a>
                    <a href="#">Shop</a>
                    <a href="#">About</a>
                    <a href="#">Contact</a>
                </div>
                <div class="footer-col">
                    <h3>Customer Service</h3>
                    <a href="#">FAQs</a>
                    <a href="#">Shipping Policy</a>
                    <a href="#">Returns & Refunds</a>
                    <a href="#">Track Order</a>
                </div>
                <div class="footer-col">
                    <h3>Contact Us</h3>
                    <p><i class="fas fa-map-marker-alt"></i> 123 Luxury Ave, Style City</p>
                    <p><i class="fas fa-phone"></i> +1 234 567 890</p>
                    <p><i class="fas fa-envelope"></i> info@luxemart.com</p>
                </div>
            </div>
            <div class="copyright">
                <p>© 2023 Shoping Mart. All Rights Reserved.</p>
            </div>
        </div>
    </footer>

    <div class="modal" id="cart-modal">
        <div class="modal-content">
            <div class="modal-header">
                <h3>Your Shopping Cart</h3>
                <button class="close-modal" id="close-modal">&times;</button>
            </div>
            <div class="cart-items" id="cart-items">
            </div>
            <div class="cart-summary">
                <div class="total">
                    <span>Total:</span>
                    <span id="cart-total">$0.00</span>
                </div>
                <button class="btn checkout-btn">Proceed to Checkout</button>
            </div>
        </div>
    </div>

    <script>
        const products = [
            {
                id: 1,
                title: "Smartphone",
                description: "Features a high-resolution touchscreen, internet connectivity, and an operating system that supports apps for communication, entertainment, productivity",
                price: 80000,
                image: "\\img\\image1.jpeg.jpg"
            },
            {
                id: 3,
                title: "novel-fiction",
                description: "well-developed characters and engaging plots that explore themes such as love, adventure, mystery, or fantasy",
                price: 199,
                image: "\\img\\novel.jpeg.jpg"
            },
            {
                id: 4,
                title: "laptop",
                description: "Equipped with powerful processors, ample storage, and long-lasting batteries, laptops are ideal for work, study, entertainment, and creative tasks",
                price: 47999,
                image: "\\img\\laptop.jpeg.jpg"
            },
            {
                id: 5,
                title: "jeans",
                description: "Durable and versatile, made from denim fabric. Known for their comfort and timeless style. Feature a fitted waistband, belt loops, and multiple pockets",
                price: 599,
                image: "\\img\\jeans.jpeg.jpg"
            },
            {
                id: 6,
                title: "cookbook",
                description: "Includes step-by-step instructions, ingredient lists, preparation times, and photographs for inspiration. Focus on dietary preferences, and skill levels",
                price: 399.,
                image: "\\img\\cookbook.jpeg.jpg"
            }
        ];
        const productsContainer = document.getElementById('products');
        const cartIcon = document.getElementById('cart-icon');
        const cartModal = document.getElementById('cart-modal');
        const closeModal = document.getElementById('close-modal');
        const cartItemsContainer = document.getElementById('cart-items');
        const cartTotal = document.getElementById('cart-total');
        const cartCount = document.querySelector('.cart-count');
        
        let cart = JSON.parse(localStorage.getItem('cart')) || [];
        function renderProducts() {
            productsContainer.innerHTML = '';
            products.forEach(product => {
                const productEl = document.createElement('div');
                productEl.classList.add('product-card');
                productEl.innerHTML = `
                    <img src="${product.image}" alt="${product.title}" class="product-img">
                    <div class="product-info">
                        <h3 class="product-title">${product.title}</h3>
                        <p class="product-desc">${product.description}</p>
                        <div class="product-price">
                            <span class="price">$${product.price.toFixed(2)}</span>
                            <button class="add-to-cart" data-id="${product.id}">Add to Cart</button>
                        </div>
                    </div>
                `;
                productsContainer.appendChild(productEl);
            });
        }
        function addToCart(id) {
            const product = products.find(item => item.id === id);
            const existingItem = cart.find(item => item.id === id);
            
            if (existingItem) {
                existingItem.quantity += 1;
            } else {
                cart.push({
                    ...product,
                    quantity: 1
                });
            }
            updateCart();
        }
        function removeFromCart(id) {
            cart = cart.filter(item => item.id !== id);
            updateCart();
        }
        function updateQuantity(id, newQuantity) {
            const item = cart.find(item => item.id === id);
            if (item) {
                item.quantity = newQuantity;
                if (item.quantity < 1) {
                    removeFromCart(id);
                } else {
                    updateCart();
                }
            }
        }
        function updateCart() {
            localStorage.setItem('cart', JSON.stringify(cart));
            const totalItems = cart.reduce((total, item) => total + item.quantity, 0);
            cartCount.textContent = totalItems;
            renderCartItems();
        }
        function renderCartItems() {
            cartItemsContainer.innerHTML = '';
            let total = 0;
            if (cart.length === 0) {
                cartItemsContainer.innerHTML = '<p>Your cart is empty</p>';
                cartTotal.textContent = '$0.00';
                return;
            }
            cart.forEach(item => {
                const itemTotal = item.price * item.quantity;
                total += itemTotal;
                const cartItemEl = document.createElement('div');
                cartItemEl.classList.add('cart-item');
                cartItemEl.innerHTML = `
                    <img src="${item.image}" alt="${item.title}" class="cart-item-img">
                    <div class="cart-item-details">
                        <h4 class="cart-item-title">${item.title}</h4>
                        <span class="cart-item-price">$${item.price.toFixed(2)}</span>
                        <div class="cart-item-quantity">
                            <button class="quantity-btn minus" data-id="${item.id}">-</button>
                            <span class="quantity">${item.quantity}</span>
                            <button class="quantity-btn plus" data-id="${item.id}">+</button>
                            <button class="remove-item" data-id="${item.id}">Remove</button>
                        </div>
                    </div>
                `;
                cartItemsContainer.appendChild(cartItemEl);
            });
            
            cartTotal.textContent = $${total.toFixed(2)};
            
            document.querySelectorAll('.minus').forEach(btn => {
                btn.addEventListener('click', (e) => {
                    const id = parseInt(e.target.dataset.id);
                    const item = cart.find(item => item.id === id);
                    if (item) {
                        updateQuantity(id, item.quantity - 1);
                    }
                });
            });
            document.querySelectorAll('.plus').forEach(btn => {
                btn.addEventListener('click', (e) => {
                    const id = parseInt(e.target.dataset.id);
                    const item = cart.find(item => item.id === id);
                    if (item) {
                        updateQuantity(id, item.quantity + 1);
                    }
                });
            });
            document.querySelectorAll('.remove-item').forEach(btn => {
                btn.addEventListener('click', (e) => {
                    const id = parseInt(e.target.dataset.id);
                    removeFromCart(id);
                });
            });
        }
        document.addEventListener('DOMContentLoaded', () => {
            renderProducts();
            renderCartItems();
            document.querySelectorAll('.add-to-cart').forEach(btn => {
                btn.addEventListener('click', (e) => {
                    const id = parseInt(e.target.dataset.id);
                    addToCart(id);
                });
            });
            cartIcon.addEventListener('click', (e) => {
                e.preventDefault();
                cartModal.style.display = 'block';
                document.body.style.overflow = 'hidden';
            });
            closeModal.addEventListener('click', () => {
                cartModal.style.display = 'none';
                document.body.style.overflow = 'auto';
            });
            window.addEventListener('click', (e) => {
                if (e.target === cartModal) {
                    cartModal.style.display = 'none';
                    document.body.style.overflow = 'auto';
                }
            });
        });
    </script>
</body>
</html>
