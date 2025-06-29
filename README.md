<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Six-X - Login</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Google Fonts - Inter -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f0f2f5; /* Light gray background */
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            padding: 1rem; /* Add some padding for smaller screens */
            box-sizing: border-box; /* Include padding in element's total width and height */
        }

        .login-container {
            background-color: #ffffff;
            padding: 2.5rem;
            border-radius: 1.5rem; /* More rounded corners */
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
            max-width: 450px; /* Slightly wider for better form layout */
            width: 100%;
            border: 6px solid transparent; /* Transparent border for gradient */
            background-clip: padding-box;
            position: relative; /* Needed for pseudo-element */
        }

        /* Colorful border effect */
        .login-container::before {
            content: '';
            position: absolute;
            inset: -6px; /* Extend border beyond padding box */
            border-radius: 1.75rem; /* Match parent's rounded corners, slightly larger */
            background: linear-gradient(
                45deg,
                #FF6B6B, /* Red */
                #FFD700, /* Gold */
                #6BFFB2, /* Light Green */
                #6B6BFF, /* Blue */
                #FF6B6B /* Red again to complete loop */
            );
            z-index: -1; /* Behind the content */
            animation: rotateGradient 10s linear infinite; /* Animation for the gradient */
            padding: 0; /* No padding for the pseudo-element itself */
        }

        @keyframes rotateGradient {
            0% { background-position: 0% 50%; }
            100% { background-position: 100% 50%; }
        }

        /* Responsive adjustments for smaller screens */
        @media (max-width: 640px) {
            .login-container {
                padding: 1.5rem;
                border-radius: 1rem;
            }
            .login-container::before {
                border-radius: 1.25rem;
            }
            h1 {
                font-size: 2rem; /* Adjust heading size */
            }
            input[type="text"],
            input[type="password"] {
                padding: 0.75rem;
            }
            button {
                padding: 0.75rem 1.5rem;
                font-size: 1rem;
            }
        }
    </style>
</head>
<body>
    <div class="login-container">
        <div class="text-center mb-8">
            <h1 class="text-5xl font-extrabold text-gray-800 tracking-tight mb-2">Six-X</h1>
            <p class="text-gray-600 text-lg">Login to your account</p>
        </div>

        <form action="#" method="POST">
            <div class="mb-5">
                <label for="email" class="block text-gray-700 text-sm font-medium mb-2">Username or Email</label>
                <input
                    type="text"
                    id="email"
                    name="email"
                    placeholder="your@example.com"
                    class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-500 focus:border-transparent transition duration-200 ease-in-out text-gray-800"
                    required
                >
            </div>

            <div class="mb-6">
                <label for="password" class="block text-gray-700 text-sm font-medium mb-2">Password</label>
                <input
                    type="password"
                    id="password"
                    name="password"
                    placeholder="••••••••"
                    class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-500 focus:border-transparent transition duration-200 ease-in-out text-gray-800"
                    required
                >
            </div>

            <button
                type="submit"
                class="w-full bg-gradient-to-r from-blue-500 to-indigo-600 text-white py-3 rounded-lg font-semibold text-lg hover:from-blue-600 hover:to-indigo-700 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:ring-offset-2 transition duration-300 ease-in-out shadow-lg"
            >
                Login
            </button>

            <div class="mt-6 text-center text-gray-600 text-sm">
                Don't have an account? <a href="#" class="text-blue-600 hover:underline font-medium">Sign Up</a>
            </div>
        </form>
    </div>
</body>
</html>
