# Amazon
This is my demo file 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>ShopKart - Home</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: Arial, sans-serif;
        }

        body {
            background: #eaeded;
        }

        /* HEADER */
        header {
            background: #131921;
            color: white;
            display: flex;
            align-items: center;
            gap: 20px;
            padding: 12px 20px;
        }

        .logo {
            font-size: 25px;
            font-weight: bold;
        }

        .logo span {
            color: #ff9900;
        }

        .search {
            flex: 1;
            display: flex;
        }

        .search input {
            width: 100%;
            padding: 12px;
            border: none;
            font-size: 16px;
        }

        .search button {
            background: #febd69;
            border: none;
            padding: 0 20px;
            cursor: pointer;
        }

        .profile-btn {
            background: transparent;
            color: white;
            border: none;
            cursor: pointer;
            font-size: 15px;
        }

        /* NAVIGATION */
        nav {
            background: #232f3e;
            color: white;
            padding: 12px 20px;
        }

        nav a {
            color: white;
            text-decoration: none;
            margin-right: 25px;
        }

        /* BANNER */
        .banner {
            background: linear-gradient(120deg, #ff9900, #ffcc66);
            padding: 45px 20px;
            text-align: center;
        }

        .banner h1 {
            font-size: 35px;
        }

        .banner p {
            margin: 10px 0 20px;
        }

        .shop-btn {
            padding: 12px 25px;
            background: #131921;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        /* PRODUCTS */
        .products {
            padding: 25px;
        }

        .products h2 {
            margin-bottom: 20px;
        }

        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 20px;
        }

        .product {
            background: white;
            padding: 15px;
            text-align: center;
            border-radius: 5px;
        }

        .product img {
            width: 100%;
            height: 180px;
            object-fit: contain;
        }

        .product h3 {
            margin: 10px 0;
        }

        .price {
            color: #b12704;
            font-size: 20px;
            font-weight: bold;
            margin-bottom: 10px;
        }

        .cart-btn {
            background: #ffd814;
            border: none;
            padding: 10px 20px;
            border-radius: 20px;
            cursor: pointer;
        }

        /* PROFILE */
        #profile {
            display: none;
            padding: 30px;
        }

        .profile-card {
            background: white;
            max-width: 500px;
            margin: auto;
            padding: 30px;
            text-align: center;
            border-radius: 10px;
        }

        .profile-img {
            width: 100px;
            height: 100px;
            border-radius: 50%;
            margin-bottom: 15px;
        }

        .profile-card h2 {
            margin-bottom: 10px;
        }

        .profile-card p {
            margin: 8px;
            color: #555;
        }

        .profile-card button {
            margin-top: 15px;
            padding: 10px 25px;
            background: #ff9900;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        /* FOOTER */
        footer {
            background: #131921;
            color: white;
            text-align: center;
            padding: 25px;
            margin-top: 30px;
        }

        @media(max-width: 600px) {
            header {
                flex-wrap: wrap;
            }

            .search {
                order: 3;
                flex-basis: 100%;
            }

            nav a {
                margin-right: 10px;
            }
        }
    </style>
</head>

<body>

    <!-- HEADER -->
    <header>

        <div class="logo">
            Shop<span>Kart</span>
        </div>

        <div class="search">
            <input type="text" placeholder="Search products...">
            <button>🔍</button>
        </div>

        <button class="profile-btn" onclick="showProfile()">
            👤 Profile
        </button>

    </header>


    <!-- NAVIGATION -->
    <nav>
        <a href="#" onclick="showHome()">Home</a>
        <a href="#products">Products</a>
        <a href="#">Orders</a>
        <a href="#">Cart 🛒</a>
    </nav>


    <!-- HOME PAGE -->
    <main id="home">

        <!-- BANNER -->
        <section class="banner">

            <h1>Welcome to ShopKart</h1>

            <p>
                Best Home Products at Amazing Prices
            </p>

            <button class="shop-btn"
                    onclick="document.getElementById('products').scrollIntoView()">
                Shop Now
            </button>

        </section>


        <!-- PRODUCTS -->
        <section class="products" id="products">

            <h2>🔥 Popular Products</h2>

            <div class="product-grid">

                <div class="product">
                    <img src="https://via.placeholder.com/300"
                         alt="Kitchen Set">

                    <h3>Kitchen Set</h3>

                    <p class="price">₹999</p>

                    <button class="cart-btn"
                            onclick="addCart('Kitchen Set')">
                        Add to Cart
                    </button>
                </div>


                <div class="product">
                    <img src="https://via.placeholder.com/300"
                         alt="Storage Box">

                    <h3>Storage Box</h3>

                    <p class="price">₹499</p>

                    <button class="cart-btn"
                            onclick="addCart('Storage Box')">
                        Add to Cart
                    </button>
                </div>


                <div class="product">
                    <img src="https://via.placeholder.com/300"
                         alt="Water Bottle">

                    <h3>Water Bottle</h3>

                    <p class="price">₹299</p>

                    <button class="cart-btn"
                            onclick="addCart('Water Bottle')">
                        Add to Cart
                    </button>
                </div>


                <div class="product">
                    <img src="https://via.placeholder.com/300"
                         alt="Cleaning Kit">

                    <h3>Cleaning Kit</h3>

                    <p class="price">₹599</p>

                    <button class="cart-btn"
                            onclick="addCart('Cleaning Kit')">
                        Add to Cart
                    </button>
                </div>

            </div>

        </section>

    </main>


    <!-- PROFILE PAGE -->
    <section id="profile">

        <div class="profile-card">

            <img class="profile-img"
                 src="https://via.placeholder.com/100"
                 alt="Profile">

            <h2>Omprasad</h2>

            <p>📧 omprasad@example.com</p>

            <p>📱 +91 XXXXX XXXXX</p>

            <p>📦 My Orders: 5</p>

            <p>🛒 Cart Items: 3</p>

            <button onclick="showHome()">
                ← Back to Home
            </button>

        </div>

    </section>


    <!-- FOOTER -->
    <footer>

        <p>© 2026 ShopKart</p>

        <p>Privacy | Terms | Customer Service</p>

    </footer>


    <!-- JAVASCRIPT -->
    <script>

        function addCart(product) {

            alert(product + " added to your cart 🛒");

        }


        function showProfile() {

            document.getElementById("home").style.display = "none";

            document.getElementById("profile").style.display = "block";

            window.scrollTo(0, 0);

        }


        function showHome() {

            document.getElementById("profile").style.display = "none";

            document.getElementById("home").style.display = "block";

            window.scrollTo(0, 0);

        }

    </script>

</body>
</html>

