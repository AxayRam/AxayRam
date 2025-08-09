<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Axay Ram - 3D GitHub Profile</title>
    <!-- Loads Tailwind CSS from CDN for modern styling -->
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        /* Import Google's "Inter" font for a clean, professional look */
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap');
        body {
            font-family: 'Inter', sans-serif;
            background-color: #0d1117; /* GitHub's dark background color */
            color: #c9d1d9; /* GitHub's light text color */
            overflow-x: hidden; /* Prevents horizontal scrolling on small screens */
            padding-bottom: 4rem; /* Adds space at the bottom */
        }
        canvas {
            display: block;
            position: fixed;
            top: 0;
            left: 0;
            z-index: -1; /* Puts the 3D canvas behind all content */
        }
        .container {
            max-width: 1024px;
            margin: 0 auto;
            padding: 2rem;
        }
        .header {
            text-align: center;
            margin-bottom: 4rem;
        }
        .section {
            background-color: #1a202c; /* A slightly different dark color for sections */
            border-radius: 1.5rem; /* More rounded corners */
            padding: 2.5rem; /* Increased padding */
            margin-bottom: 2rem;
            border: 1px solid #4a5568; /* A darker, more subtle border */
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3); /* Stronger shadow */
            transition: transform 0.3s ease-in-out, box-shadow 0.3s ease-in-out;
        }
        .section:hover {
            transform: translateY(-10px); /* More pronounced lift on hover */
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.4);
        }
        .project-card {
            background-color: #2d3748; /* A shade lighter than the section */
            border-radius: 1rem;
            padding: 2rem;
            border: 1px solid #4a5568;
            transition: box-shadow 0.3s ease-in-out, transform 0.3s ease-in-out;
        }
        .project-card:hover {
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3);
            transform: scale(1.02);
        }
        .skill-badge {
            background-color: #4c51bf; /* A vibrant purple color for skill badges */
            color: white;
            padding: 0.75rem 1.5rem; /* Larger badges for readability */
            border-radius: 9999px;
            font-size: 1rem;
            font-weight: 600;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }
        /* Keyframes for a more subtle fade-in animation */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(30px); }
            to { opacity: 1; transform: translateY(0); }
        }
        .animate-fadeIn {
            animation: fadeIn 1s ease-out forwards;
        }
        /* Style for the social links */
        .social-link {
            transition: color 0.3s ease-in-out;
            font-size: 1.125rem;
            text-decoration: none;
            font-weight: 600;
        }
    </style>
</head>
<body>

    <!-- Canvas element for the interactive 3D background animation -->
    <canvas id="bg-canvas"></canvas>

    <div class="container mx-auto px-4 py-8">

        <!-- Header Section -->
        <header class="header animate-fadeIn">
            <h1 class="text-6xl font-extrabold text-white mb-4">AXAY RAM 👋</h1>
            <p class="text-2xl text-[#a0aec0] font-light">
                🎓 Electronics & Communication Engineering Student | 💻 Embedded Systems & Firmware Developer
            </p>
            <div class="mt-8 flex flex-wrap justify-center space-x-4 text-white">
                <a href="https://github.com/AxayRam" target="_blank" class="social-link hover:text-[#58a6ff]">🌐 GitHub</a>
                <a href="https://www.linkedin.com/in/ram-axay" target="_blank" class="social-link hover:text-[#58a6ff]">💼 LinkedIn</a>
                <a href="mailto:axay19392@gmail.com" class="social-link hover:text-[#58a6ff]">✉️ Email</a>
            </div>
        </header>

        <!-- Programming Languages & Tools Section -->
        <section class="section animate-fadeIn" style="animation-delay: 0.2s;">
            <h2 class="text-4xl font-bold mb-6 text-white">Programming Languages & Tools</h2>
            <div class="flex flex-wrap gap-4 justify-center">
                <span class="skill-badge">C ✅</span>
                <span class="skill-badge">Embedded C</span>
                <span class="skill-badge">Assembly (8086, ARM7)</span>
                <span class="skill-badge">GCC</span>
                <span class="skill-badge">GDB</span>
                <span class="skill-badge">GNU Make</span>
                <span class="skill-badge">STM32</span>
                <span class="skill-badge">ESP32</span>
                <span class="skill-badge">Arduino</span>
                <span class="skill-badge">Linux Terminal</span>
                <span class="skill-badge">Git</span>
            </div>
        </section>

        <!-- Projects Section -->
        <section class="section animate-fadeIn" style="animation-delay: 0.4s;">
            <h2 class="text-4xl font-bold mb-6 text-white">Projects</h2>
            <div class="grid md:grid-cols-2 gap-8">
                <!-- Project: Raspberry Pi 5 -->
                <div class="project-card">
                    <h3 class="text-2xl font-semibold mb-2 text-white">🔴 Raspberry Pi 5 (C + Linux)</h3>
                    <ul class="list-disc list-inside text-[#a0aec0] space-y-1">
                        <li>✅ LED Blinking via GPIO in C</li>
                        <li>✅ Ultrasonic Sensor Distance Calculation with C</li>
                    </ul>
                </div>
                <!-- Project: ESP32-CAM -->
                <div class="project-card">
                    <h3 class="text-2xl font-semibold mb-2 text-white">📷 ESP32-CAM</h3>
                    <p class="text-[#a0aec0]">✅ Wireless Surveillance System using Telegram Bot → Sends live image snapshots to Telegram for monitoring</p>
                </div>
                <!-- Project: Signal Processing -->
                <div class="project-card">
                    <h3 class="text-2xl font-semibold mb-2 text-white">🔊 Signal Processing</h3>
                    <p class="text-[#a0aec0]">✅ Pulse Code Modulation Generator in C → Generates .raw sinewave PCM file, verified in Audacity</p>
                </div>
                <!-- Project: Women Safety Device -->
                <div class="project-card">
                    <h3 class="text-2xl font-semibold mb-2 text-white">📿 Women Safety Device</h3>
                    <p class="text-[#a0aec0]">✅ GSM + GPS + Keypad + EEPROM integration → Sends SMS with location, emergency calling on button press</p>
                </div>
            </div>
        </section>

        <!-- Certifications Section -->
        <section class="section animate-fadeIn" style="animation-delay: 0.6s;">
            <h2 class="text-4xl font-bold mb-6 text-white">Certifications</h2>
            <ul class="list-disc list-inside text-[#a0aec0] space-y-2">
                <li>C Programming – Bharat Acharya Education</li>
                <li>8086 Microprocessor – Bharat Acharya Education</li>
                <li>ARM7 Microcontroller – Bharat Acharya Education</li>
                <li>ARM Cortex-M 101 & 102 – Pyjama Brah</li>
                <li>C Mastery, Pointers, Bit Manipulation, DSA – Pyjama Brah</li>
                <li>GNU Makefile & Automation – Pyjama Brah</li>
                <li>Introduction to C on Raspberry Pi – Udemy</li>
            </ul>
        </section>

        <!-- Connect Section -->
        <section class="section animate-fadeIn" style="animation-delay: 0.8s;">
            <h2 class="text-4xl font-bold mb-6 text-white">Connect With Me</h2>
            <p class="mb-4 text-center text-[#a0aec0] text-xl font-semibold">
                ⚡ Passionate about Embedded Systems, Bare-Metal Programming, and Low-level C Development. Always building, always learning!
            </p>
            <div class="flex flex-col md:flex-row md:space-x-8 space-y-4 md:space-y-0 justify-center text-white">
                <a href="mailto:axay19392@gmail.com" class="social-link hover:text-[#58a6ff]">✉️ Email : axay19392@gmail.com</a>
                <a href="https://github.com/AxayRam" target="_blank" class="social-link hover:text-[#58a6ff]">🌐 GitHub : github.com/AxayRam</a>
                <a href="https://linkedin.com/in/ram-axay" target="_blank" class="social-link hover:text-[#58a6ff]">💼 LinkedIn : linkedin.com/in/ram-axay</a>
            </div>
        </section>
    </div>
    
    <!-- JavaScript libraries and custom script are loaded here -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
    <script>
        // This script handles the interactive 3D background animation using Three.js
        window.onload = function() {
            // 1. Scene, camera, and renderer setup
            // The scene is the main container for all objects, lights, and cameras.
            const scene = new THREE.Scene();
            // The camera defines what the user sees. The parameters are: Field of View, Aspect Ratio, Near Clipping Plane, Far Clipping Plane.
            const camera = new THREE.PerspectiveCamera(75, window.innerWidth / window.innerHeight, 0.1, 1000);
            // The renderer handles drawing the scene onto the canvas. `alpha: true` makes the background transparent.
            const renderer = new THREE.WebGLRenderer({ canvas: document.getElementById('bg-canvas'), antialias: true, alpha: true });
            renderer.setSize(window.innerWidth, window.innerHeight);
            renderer.setClearColor(0x0d1117, 0); // Sets the clear color to transparent

            // 2. Create the objects (cubes) for the background
            const geometry = new THREE.BoxGeometry(0.5, 0.5, 0.5); // Defines the shape of the cubes
            const material = new THREE.MeshBasicMaterial({ color: 0x4c51bf, wireframe: true }); // Defines the appearance (vibrant purple wireframe)
            const cubes = [];
            // Create and position 50 cubes randomly in a large area
            for (let i = 0; i < 50; i++) {
                const cube = new THREE.Mesh(geometry, material);
                cube.position.set(
                    (Math.random() - 0.5) * 50,
                    (Math.random() - 0.5) * 50,
                    (Math.random() - 0.5) * 50
                );
                cubes.push(cube);
                scene.add(cube);
            }
            camera.position.z = 5; // Position the camera to see the cubes

            // 3. Handle window resizing to keep the animation responsive
            window.addEventListener('resize', () => {
                camera.aspect = window.innerWidth / window.innerHeight;
                camera.updateProjectionMatrix();
                renderer.setSize(window.innerWidth, window.innerHeight);
            }, false);

            // 4. Animation loop for continuous automatic rotation
            const animate = () => {
                // `requestAnimationFrame` tells the browser to perform an animation and calls the function again
                requestAnimationFrame(animate);

                // Rotate each cube slightly on every frame
                cubes.forEach(cube => {
                    cube.rotation.x += 0.005;
                    cube.rotation.y += 0.005;
                });

                // Render the scene from the camera's perspective
                renderer.render(scene, camera);
            };
            animate();

            // 5. Add interactivity: mouse movement rotates the cubes
            let mouseX = 0, mouseY = 0;
            let targetX = 0, targetY = 0;
            const windowHalfX = window.innerWidth / 2;
            const windowHalfY = window.innerHeight / 2;

            // Update mouse coordinates when the mouse moves
            document.addEventListener('mousemove', (event) => {
                mouseX = (event.clientX - windowHalfX);
                mouseY = (event.clientY - windowHalfY);
            });

            // Update the cube rotations based on the mouse position
            function updateCubes() {
                targetX = mouseX * 0.001;
                targetY = mouseY * 0.001;
                
                if (cubes.length > 0) {
                    cubes.forEach(cube => {
                        // Smoothly interpolate the rotation towards the target
                        cube.rotation.x += 0.05 * (targetY - cube.rotation.x);
                        cube.rotation.y += 0.05 * (targetX - cube.rotation.y);
                    });
                }
            }

            // The main interactive animation loop
            const interactiveAnimate = () => {
                requestAnimationFrame(interactiveAnimate);
                updateCubes();
                renderer.render(scene, camera);
            };
            interactiveAnimate();
        };
    </script>
</body>
</html>
