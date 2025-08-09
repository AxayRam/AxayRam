<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Axay Ram - Portfolio</title>
    <!-- Loads Tailwind CSS from CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        /* Import Google Font "Inter" */
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap');
        body {
            font-family: 'Inter', sans-serif;
            background-color: #0d1117; /* Dark background color */
            color: #c9d1d9; /* Light text color */
            overflow-x: hidden; /* Prevents horizontal scrolling */
        }
        canvas {
            display: block;
            position: fixed;
            top: 0;
            left: 0;
            z-index: -1; /* Ensures the canvas is behind all other content */
        }
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 2rem;
        }
        .header {
            text-align: center;
            margin-bottom: 4rem;
        }
        .section {
            background-color: #161b22;
            border-radius: 1rem;
            padding: 2rem;
            margin-bottom: 2rem;
            border: 1px solid #30363d;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease-in-out;
        }
        .section:hover {
            transform: translateY(-5px); /* Adds a subtle lift effect on hover */
        }
        .project-card {
            background-color: #0d1117;
            border-radius: 0.75rem;
            padding: 1.5rem;
            border: 1px solid #30363d;
            transition: box-shadow 0.3s ease-in-out, transform 0.3s ease-in-out;
        }
        .project-card:hover {
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
            transform: scale(1.02);
        }
        .skill-badge {
            background-color: #21262d;
            color: #58a6ff;
            padding: 0.5rem 1rem;
            border-radius: 9999px;
            font-size: 0.875rem;
            font-weight: 600;
        }
        /* Keyframes for the fade-in animation */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        .animate-fadeIn {
            animation: fadeIn 1s ease-out forwards;
        }
    </style>
</head>
<body>

    <!-- Canvas element for the interactive 3D background animation -->
    <canvas id="bg-canvas"></canvas>

    <div class="container mx-auto px-4 py-8">

        <!-- Header Section -->
        <header class="header animate-fadeIn">
            <h1 class="text-5xl font-bold text-white mb-2">AXAY RAM</h1>
            <p class="text-xl text-[#8b949e]">Electronics & Communication Engineering Student | Embedded Systems & Firmware Developer</p>
            <div class="mt-4 flex justify-center space-x-4 text-white">
                <a href="https://github.com/AxayRam" target="_blank" class="hover:text-[#58a6ff] transition-colors duration-200">GitHub</a>
                <a href="https://www.linkedin.com/in/ram-axay" target="_blank" class="hover:text-[#58a6ff] transition-colors duration-200">LinkedIn</a>
                <a href="mailto:axay19392@gmail.com" class="hover:text-[#58a6ff] transition-colors duration-200">Email</a>
            </div>
        </header>

        <!-- Programming Languages Section -->
        <section class="section animate-fadeIn" style="animation-delay: 0.2s;">
            <h2 class="text-3xl font-bold mb-4 text-white">Programming Languages</h2>
            <div class="flex flex-wrap gap-2">
                <span class="skill-badge">C ✅</span>
                <span class="skill-badge">Embedded C (Bare-Metal, Drivers)</span>
                <span class="skill-badge">Assembly (8086, ARM7 basics)</span>
            </div>
        </section>

        <!-- Frameworks, Tools & Libraries Section -->
        <section class="section animate-fadeIn" style="animation-delay: 0.4s;">
            <h2 class="text-3xl font-bold mb-4 text-white">Frameworks, Tools & Libraries</h2>
            <div class="flex flex-wrap gap-2">
                <span class="skill-badge">GCC</span>
                <span class="skill-badge">GDB</span>
                <span class="skill-badge">GNU Make</span>
                <span class="skill-badge">Linker Scripts</span>
                <span class="skill-badge">STM32 (ARM Cortex-M)</span>
                <span class="skill-badge">ESP32</span>
                <span class="skill-badge">Arduino</span>
                <span class="skill-badge">Linux Terminal</span>
                <span class="skill-badge">Shell</span>
                <span class="skill-badge">VS Code</span>
                <span class="skill-badge">Git</span>
                <span class="skill-badge">GitHub</span>
            </div>
        </section>

        <!-- Projects Section -->
        <section class="section animate-fadeIn" style="animation-delay: 0.6s;">
            <h2 class="text-3xl font-bold mb-4 text-white">Projects</h2>
            <div class="grid md:grid-cols-2 gap-6">
                <!-- Project: Raspberry Pi 5 -->
                <div class="project-card">
                    <h3 class="text-xl font-semibold mb-2 text-white">🔴 Raspberry Pi 5 (C + Linux)</h3>
                    <ul class="list-disc list-inside text-[#8b949e] space-y-1">
                        <li>LED Blinking via GPIO in C</li>
                        <li>Ultrasonic Sensor Distance Calculation with C</li>
                    </ul>
                </div>
                <!-- Project: ESP32-CAM -->
                <div class="project-card">
                    <h3 class="text-xl font-semibold mb-2 text-white">📷 ESP32-CAM</h3>
                    <p class="text-[#8b949e]">Wireless Surveillance System using Telegram Bot → Sends live image snapshots to Telegram for monitoring</p>
                </div>
                <!-- Project: Signal Processing -->
                <div class="project-card">
                    <h3 class="text-xl font-semibold mb-2 text-white">🔊 Signal Processing</h3>
                    <p class="text-[#8b949e]">Pulse Code Modulation Generator in C → Generates .raw sinewave PCM file, verified in Audacity</p>
                </div>
                <!-- Project: Women Safety Device -->
                <div class="project-card">
                    <h3 class="text-xl font-semibold mb-2 text-white">📿 Women Safety Device</h3>
                    <p class="text-[#8b949e]">GSM + GPS + Keypad + EEPROM integration → Sends SMS with location, emergency calling on button press</p>
                </div>
            </div>
        </section>

        <!-- Certifications Section -->
        <section class="section animate-fadeIn" style="animation-delay: 0.8s;">
            <h2 class="text-3xl font-bold mb-4 text-white">Certifications</h2>
            <ul class="list-disc list-inside text-[#8b949e] space-y-1">
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
        <section class="section animate-fadeIn" style="animation-delay: 1.0s;">
            <h2 class="text-3xl font-bold mb-4 text-white">Connect With Me</h2>
            <div class="flex flex-col md:flex-row md:space-x-4 space-y-2 md:space-y-0 justify-center text-white">
                <a href="mailto:axay19392@gmail.com" class="hover:text-[#58a6ff] transition-colors duration-200">✉️ Email : axay19392@gmail.com</a>
                <a href="https://github.com/AxayRam" target="_blank" class="hover:text-[#58a6ff] transition-colors duration-200">🌐 GitHub : github.com/AxayRam</a>
                <a href="https://linkedin.com/in/your-linkedin-ram-axay" target="_blank" class="hover:text-[#58a6ff] transition-colors duration-200">💼 LinkedIn : linkedin.com/in/ram-axay</a>
            </div>
            <p class="mt-4 text-center text-[#8b949e] text-lg font-semibold">
                ⚡ Passionate about Embedded Systems, Bare-Metal Programming, and Low-level C Development. Always building, always learning!
            </p>
        </section>

    </div>
    
    <!-- JavaScript libraries and custom script are loaded here -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
    <script>
        // Three.js 3D Background Animation
        window.onload = function() {
            // 1. Scene, camera, and renderer setup
            const scene = new THREE.Scene();
            const camera = new THREE.PerspectiveCamera(75, window.innerWidth / window.innerHeight, 0.1, 1000);
            const renderer = new THREE.WebGLRenderer({ canvas: document.getElementById('bg-canvas'), antialias: true, alpha: true });
            renderer.setSize(window.innerWidth, window.innerHeight);
            renderer.setClearColor(0x0d1117, 0);

            // 2. Create the cubes
            const geometry = new THREE.BoxGeometry(0.5, 0.5, 0.5);
            const material = new THREE.MeshBasicMaterial({ color: 0x58a6ff, wireframe: true });
            const cubes = [];
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

            camera.position.z = 5;

            // 3. Handle window resize event to maintain responsiveness
            window.addEventListener('resize', () => {
                camera.aspect = window.innerWidth / window.innerHeight;
                camera.updateProjectionMatrix();
                renderer.setSize(window.innerWidth, window.innerHeight);
            }, false);

            // 4. Animation loop for continuous automatic rotation
            const animate = () => {
                requestAnimationFrame(animate);

                cubes.forEach(cube => {
                    cube.rotation.x += 0.005;
                    cube.rotation.y += 0.005;
                });

                renderer.render(scene, camera);
            };

            animate();

            // 5. Interactive element: mouse movement rotates the cubes
            let mouseX = 0, mouseY = 0;
            let targetX = 0, targetY = 0;
            const windowHalfX = window.innerWidth / 2;
            const windowHalfY = window.innerHeight / 2;

            document.addEventListener('mousemove', (event) => {
                mouseX = (event.clientX - windowHalfX);
                mouseY = (event.clientY - windowHalfY);
            });

            function updateCamera() {
                targetX = mouseX * 0.001;
                targetY = mouseY * 0.001;
                
                if (cubes.length > 0) {
                    cubes.forEach(cube => {
                        cube.rotation.x += 0.05 * (targetY - cube.rotation.x);
                        cube.rotation.y += 0.05 * (targetX - cube.rotation.y);
                    });
                }
            }

            const interactiveAnimate = () => {
                requestAnimationFrame(interactiveAnimate);
                updateCamera();
                renderer.render(scene, camera);
            };
            interactiveAnimate();
        };
    </script>
</body>
</html>
