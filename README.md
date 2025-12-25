# Project Responsive Web Design using Bootstrap
# Date:
22.12.2025
# AIM:
To create a simplified clone of Dribbble (https://dribbble.com/) landing page.

# DESIGN STEPS:
## Step 1:
Clone the repository from GitHub.

## Step 2:
Create Django Admin project.

## Step 3:
Create a New App under the Django Admin project.

## Step 4:
Insert the necessary CSS and JavaScript files as external in order to use Bootstrap.

## Step 5:
Create a HTML file and include the needed Bootstrap components.

## Step 6:
Publish the website in the LocalHost.

# PROGRAM :
```
views.py

from django.shortcuts import render

def home(request):
    return render(request, 'index.html')

def support(request):
    return render(request, 'support.html')

def signin(request):
    return render(request, 'signin.html')

def uiux(request):
    return render(request, 'uiux.html')

def hire(request):
    return render(request, 'hire.html')

def inspiration(request):
    return render(request, 'inspiration.html')

def getstarted(request):
    return render(request, 'getstarted.html')

def creative(request):
    return render(request, 'creative.html')

def design(request):
    return render(request, 'design.html')

def portfolio(request):
    return render(request, 'portfolio.html')

urls.py

from django.contrib import admin
from django.urls import path
from myapp import views

urlpatterns = [
    path('admin/', admin.site.urls),
    path('', views.home, name='home'),
    path('support/', views.support, name='support'),
    path('signin/', views.signin, name='signin'),
    path('sign/', views.signin),
    path('getstarted/', views.getstarted, name='getstarted'),


    # Service pages
    path('uiux/', views.uiux, name='uiux'),
    path('hire/', views.hire, name='hire'),
    path('inspiration/', views.inspiration, name='inspiration'),
    path('design/', views.design, name='design'),
    path('learning/', views.design, name='design'),
    path('creative/', views.creative, name='creative'),
    path('portfolio/', views.portfolio, name='portfolio'),
]

index.html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Dribbble Clone</title>

    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">

    <style>
        body {
            font-family: 'Segoe UI', sans-serif;
            background-color: #f8f9fa;
        }

        /* Navbar */
        .navbar-brand {
            font-weight: bold;
            color: #ea4c89 !important;
            font-size: 1.6rem;
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, #fde4ec, #f8cdda);
            padding: 100px 20px;
            text-align: center;
        }

        .hero h1 {
            font-size: 3rem;
            font-weight: 700;
            color: #1f1f1f;
        }

        .hero p {
            font-size: 1.1rem;
            color: #555;
            margin-top: 15px;
        }

        .hero .btn {
            background-color: #1f1f1f;
            color: white;
            padding: 12px 28px;
            border-radius: 30px;
            margin-top: 20px;
        }

        /* Trending Section */
        .section-title {
            text-align: center;
            margin: 60px 0 30px;
            font-weight: 600;
        }

        /* Service Cards */
        .service-card {
            border-radius: 18px;
            padding: 30px;
            background: white;
            box-shadow: 0 8px 20px rgba(0,0,0,0.08);
            transition: transform 0.3s ease;
            height: 100%;
        }

        .service-card:hover {
            transform: translateY(-8px);
        }

        .service-icon {
            font-size: 2.5rem;
            color: #ea4c89;
        }

        .service-card h5 {
            margin-top: 15px;
            font-weight: 600;
        }

        .service-card p {
            color: #666;
            font-size: 0.95rem;
        }
    </style>
</head>
<body>

<!-- Navbar -->
<!-- Navbar -->
<nav class="navbar navbar-expand-lg bg-white shadow-sm">
    <div class="container">
        <a class="navbar-brand fw-bold" style="color:#ea4c89" href="/">dribbble</a>

        <button class="navbar-toggler" data-bs-toggle="collapse" data-bs-target="#navMenu">
            <span class="navbar-toggler-icon"></span>
        </button>

        <div class="collapse navbar-collapse" id="navMenu">
            <ul class="navbar-nav ms-auto align-items-center">
                <li class="nav-item">
                    <a class="nav-link" href="/support/">Support</a>
                </li>
                <li class="nav-item">
                    <a class="btn btn-outline-dark ms-3" href="/signin/">Sign In</a>
                </li>
            </ul>
        </div>
    </div>
</nav>


<!-- Hero Section -->
<section class="hero">
    <h1>Discover the world’s top designers<br>& creatives</h1>
    <p>The best place to explore and showcase creative work</p>
    <a href="/getstarted/" class="btn">Get Started</a>
</section>

<!-- Trending Services -->
<div class="row g-4">

    <div class="col-md-4">
        <a href="/uiux/" class="text-decoration-none text-dark">
            <div class="service-card text-center">
                <div class="service-icon">🎨</div>
                <h5>UI / UX Design</h5>
                <p>Modern interfaces, mobile apps, and web experiences.</p>
            </div>
        </a>
    </div>

    <div class="col-md-4">
        <a href="/hire/" class="text-decoration-none text-dark">
            <div class="service-card text-center">
                <div class="service-icon">💼</div>
                <h5>Hire Designers</h5>
                <p>Find top designers for freelance and full-time roles.</p>
            </div>
        </a>
    </div>

    <div class="col-md-4">
        <a href="/inspiration/" class="text-decoration-none text-dark">
            <div class="service-card text-center">
                <div class="service-icon">🚀</div>
                <h5>Design Inspiration</h5>
                <p>Explore trending creative ideas and portfolios.</p>
            </div>
        </a>
    </div>

</div>

signin.html

<!DOCTYPE html>
<html>
<head>
    <title>Sign In | Dribbble</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">
</head>

<body class="bg-light">

<div class="container mt-5">
    <div class="card shadow p-4 mx-auto" style="max-width:400px;">
        <h3 class="text-center mb-3">Sign In</h3>
        <p class="text-muted text-center">Welcome back!</p>

        <form>
            <div class="mb-3">
                <label>Email</label>
                <input type="email" class="form-control" required>
            </div>

            <div class="mb-3">
                <label>Password</label>
                <input type="password" class="form-control" required>
            </div>

            <button class="btn btn-dark w-100">Sign In</button>
        </form>
    </div>
</div>

</body>
</html>

support.html

<!DOCTYPE html>
<html>
<head>
    <title>Support | Dribbble</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">
</head>

<body class="bg-light">

<div class="container mt-5">
    <div class="card shadow p-4 mx-auto" style="max-width:500px;">
        <h3 class="text-center mb-3">Support Center</h3>
        <p class="text-muted text-center">Need help? Contact our support team</p>

        <form>
            <div class="mb-3">
                <label>Name</label>
                <input type="text" class="form-control" required>
            </div>

            <div class="mb-3">
                <label>Email</label>
                <input type="email" class="form-control" required>
            </div>

            <div class="mb-3">
                <label>Your Issue</label>
                <textarea class="form-control" rows="4"></textarea>
            </div>

            <button class="btn btn-dark w-100">Submit Request</button>
        </form>
    </div>
</div>

</body>
</html>

getstarted.html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Get Started | Dribbble</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">

    <style>
        body {
            background-color: #f8f9fa;
        }
        .service-card {
            background: white;
            border-radius: 16px;
            padding: 25px;
            box-shadow: 0 8px 20px rgba(0,0,0,0.08);
            transition: transform 0.3s;
            height: 100%;
        }
        .service-card:hover {
            transform: translateY(-6px);
        }
        .icon {
            font-size: 2rem;
        }
    </style>
</head>
<body>

<div class="container mt-5">

    <h2 class="text-center mb-4">Get Started with Dribbble</h2>
    <p class="text-center text-muted mb-5">
        Choose a service below to begin your creative journey
    </p>

    <div class="row g-4">

        <!-- COLUMN 1 -->
        <div class="col-md-4">
            <a href="/uiux/" class="text-decoration-none text-dark">
                <div class="service-card text-center">
                    <div class="icon">🎨</div>
                    <h5 class="mt-3">UI / UX Design</h5>
                    <p>Design modern interfaces and experiences.</p>
                </div>
            </a>

            <a href="/portfolio/" class="text-decoration-none text-dark">
                <div class="service-card text-center mt-4">
                    <div class="icon">📢</div>
                    <h5 class="mt-3">Portfolio Showcase</h5>
                    <p>Showcase your creative work globally.</p>
                </div>
            </a>
        </div>

        <!-- COLUMN 2 -->
        <div class="col-md-4">
            <a href="/hire/" class="text-decoration-none text-dark">
                <div class="service-card text-center">
                    <div class="icon">💼</div>
                    <h5 class="mt-3">Hire Designers</h5>
                    <p>Find professional designers easily.</p>
                </div>
            </a>

            <a href="/design/" class="text-decoration-none text-dark">
                <div class="service-card text-center mt-4">
                    <div class="icon">📚</div>
                    <h5 class="mt-3">Design Learning</h5>
                    <p>Learn skills from industry experts.</p>
                </div>
            </a>
        </div>

        <!-- COLUMN 3 -->
        <div class="col-md-4">
            <a href="/inspiration/" class="text-decoration-none text-dark">
                <div class="service-card text-center">
                    <div class="icon">🚀</div>
                    <h5 class="mt-3">Design Inspiration</h5>
                    <p>Explore trending creative ideas.</p>
                </div>
            </a>

            <a href="/creative/" class="text-decoration-none text-dark">
                <div class="service-card text-center mt-4">
                    <div class="icon">🌍</div>
                    <h5 class="mt-3">Creative Community</h5>
                    <p>Connect with creatives worldwide.</p>
                </div>
            </a>
        </div>

    </div>

    <div class="text-center mt-5">
        <a href="/" class="btn btn-dark">Back to Home</a>
    </div>

</div>

</body>
</html>

uiux.html

<!DOCTYPE html>
<html>
<head>
    <title>UI / UX Design</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">
</head>

<body class="bg-light">
<div class="container mt-5">
    <div class="card shadow p-4">
        <h2>UI / UX Design</h2>
        <p class="text-muted">Create beautiful and user-friendly interfaces.</p>
        <p>
            Dribbble helps designers showcase UI and UX projects including
            mobile apps, websites, dashboards, and design systems.
        </p>
        <a href="/" class="btn btn-dark">Back to Home</a>
    </div>
</div>
</body>
</html>

hire.html

<!DOCTYPE html>
<html>
<head>
    <title>Hire Designers</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">
</head>

<body class="bg-light">
<div class="container mt-5">
    <div class="card shadow p-4">
        <h2>Hire Designers</h2>
        <p class="text-muted">Find professional designers easily.</p>
        <p>
            Companies can hire designers for freelance, contract,
            remote, or full-time positions through Dribbble.
        </p>
        <a href="/" class="btn btn-dark">Back to Home</a>
    </div>
</div>
</body>
</html>

inspiration.html

<!DOCTYPE html>
<html>
<head>
    <title>Design Inspiration</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">
</head>

<body class="bg-light">
<div class="container mt-5">
    <div class="card shadow p-4">
        <h2>Design Inspiration</h2>
        <p class="text-muted">Explore creative trends worldwide.</p>
        <p>
            Designers share branding, illustration, animation, and UI ideas
            to inspire others in the creative community.
        </p>
        <a href="/" class="btn btn-dark">Back to Home</a>
    </div>
</div>
</body>
</html>

design.html

<!DOCTYPE html>
<html>
<head>
    <title>Design Learning</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">
</head>

<body class="bg-light">
<div class="container mt-5">
    <div class="card shadow p-4">
        <h2>Learn Designing</h2>
        <p class="text-muted">Learn how to design professionally</p>
        <p>
            Tired of spending so much on designers?
            Learn how to design all by yourself.
        </p>
        <a href="/" class="btn btn-dark">Back to Home</a>
    </div>
</div>
</body>
</html>

creative.html

<!DOCTYPE html>
<html>
<head>
    <title>Creative Community</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">
</head>

<body class="bg-light">
<div class="container mt-5">
    <div class="card shadow p-4">
        <h2>Creative Community</h2>
        <p class="text-muted">Find a Creative Community where you belong</p>
        <p>
            The world is full of people with creative ideas and mindsets.
            Here you can find your type of people.
        </p>
        <a href="/" class="btn btn-dark">Back to Home</a>
    </div>
</div>
</body>
</html>

portfolio.html

<!DOCTYPE html>
<html>
<head>
    <title>Portfolio Showcase</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">
</head>

<body class="bg-light">
<div class="container mt-5">
    <div class="card shadow p-4">
        <h2>Portfolio Showcase</h2>
        <p class="text-muted">Show your Portfolios and see others too</p>
        <p>
            Do you want to show your portfolios?
            Here is the right place.
        </p>
        <a href="/" class="btn btn-dark">Back to Home</a>
    </div>
</div>
</body>
</html>
```

# OUTPUT:
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/1ee14bd3-914c-4657-a198-9f67c19fccac" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/2142fb57-1601-42ef-bc72-0b2c979f8223" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/357f17dd-2c83-428f-8cf6-5346f2fefb89" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/5f0fd312-84a8-4a36-9206-eefe332d3bc3" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/007525c2-e444-4a83-94ed-68d6227f4d2e" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/7a6807b9-8348-493a-8c30-65f56a5073d0" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/e5896562-49f7-403a-8048-b63121005ff6" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/c4fec941-1faa-4e60-ac20-307c86dd32be" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/60521e5b-5562-4efa-b321-60561ae4021d" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/9314afe4-44ca-449e-9ddf-e151e90cefa2" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/b0e199e1-4e07-4ce3-a234-7bd1f60a6f74" />

# RESULT:
The Project for responsive web design using Bootstrap is completed successfully.
