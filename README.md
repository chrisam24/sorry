<html lang="en">
<head>
    <meta charset="utf-8"/>
    <meta content="width=device-width, initial-scale=1.0" name="viewport"/>
    <title>Love Message</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css" rel="stylesheet"/>
    <link href="https://fonts.googleapis.com/css2?family=Great+Vibes&display=swap" rel="stylesheet"/>
    <style>
        body {
            font-family: 'Times New Roman', Times, serif;
        }
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        @keyframes beat {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.2); }
        }
        @keyframes break {
            0% { transform: scale(1); }
            50% { transform: scale(1.2); }
            100% { transform: scale(0); opacity: 0; }
        }
        .fade-in {
            animation: fadeIn 1s ease-in-out;
        }
        .beat {
            animation: beat 1s infinite;
        }
        .break {
            animation: break 1s forwards;
        }
    </style>
</head>
<body class="bg-pink-50 flex items-center justify-center min-h-screen">
    <div id="loginPage" class="w-full max-w-xs">
        <form class="bg-white shadow-md rounded px-8 pt-6 pb-8 mb-4">
            <h2 class="text-2xl text-center text-pink-600 mb-4">Login</h2>
            <div class="mb-4">
                <label class="block text-gray-700 text-sm font-bold mb-2" for="username">
                    Username
                </label>
                <input class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="username" type="text" placeholder="Username">
            </div>
            <div class="mb-6">
                <label class="block text-gray-700 text-sm font-bold mb-2" for="password">
                    Password
                </label>
                <input class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 mb-3 leading-tight focus:outline-none focus:shadow-outline" id="password" type="password" placeholder="******************">
            </div>
            <div class="flex items-center justify-between">
                <button class="bg-pink-500 hover:bg-pink-700 text-white font-bold py-2 px-4 rounded focus:outline-none focus:shadow-outline" type="button" id="loginButton">
                    Login
                </button>
            </div>
        </form>
    </div>

    <div id="messagePage" class="hidden text-center p-6 bg-white shadow-lg rounded-lg relative">
        <img alt="A beautiful arrangement of white flowers" class="absolute inset-0 w-full h-full object-cover opacity-20" height="400" src="https://storage.googleapis.com/a1aa/image/l5nzfgaX2S18aSNzcyTG9hWMfdzM3iDsKsWtUTFAgeZW5cEoA.jpg" width="600"/>
        <div class="relative z-10">
            <button class="text-red-600 text-4xl mb-4" id="envelopeButton">
                <i class="fas fa-envelope"></i>
            </button>
            <div id="messageContent" class="hidden fade-in">
                <h1 class="text-4xl text-pink-600 mb-4">Hi Love,</h1>
                <p class="text-lg text-gray-700 mb-4">
                    I know I’ve made so many mistakes, and every time I think about it, my heart breaks. I’ve hurt you deeply, and I can’t take that back. I know I’m not the same person you once met, and it’s painful to admit that I’ve changed in ways that caused you so much hurt. I take full responsibility for everything I did, and I’m so sorry, love. I know saying sorry might not heal your broken heart, and I carry that guilt with me every day. There’s no need for you to bring up what I did, because I already feel the weight of it all. I know how much it’s impacted our relationship, and it’s hard to even find the words to express how much I regret causing you pain. I know you’re tired of me, and I understand. I never wanted to be the source of your pain. I don’t want to make any more promises or say anything I can’t keep. I know I’ve been unfair to you. You’ve always given your best in this relationship, while I kept making mistake after mistake. I see now how hard that must have been for you, and I’m so sorry. I understand if you doubt whether I deserve another chance. I would feel the same way, and I can’t blame you for it. I’m sorry for everything, from the bottom of my heart. I’m not tired because of us or the relationship—it’s just that I’m worn out from all the mistakes I made. I wish I could fix everything, but I can’t. Please know that I love you more than words can express. One thing I ask, love: please always check in on my mom whenever she feels alone. She needs your support, and I can’t be there for her like I should have been. I love you so much, and I’m so sorry for everything. If I could make things right, I would. I hope, somehow, you can find it in your heart to forgive me. This may be my first flower to receive, and I would be so grateful if my circle of friends could be there.
                </p>
                <p class="text-lg text-gray-700 mb-4">
                    I love you, always and forever
                </p>
                <button class="text-pink-600 text-4xl beat" id="playButton">
                    <i class="fas fa-heart"></i>
                </button>
            </div>
        </div>
    </div>

    <audio id="loveSong" src="https://www.example.com/ikaw-lang-nobita.mp3"></audio>

    <script>
        document.getElementById('loginButton').addEventListener('click', function() {
            document.getElementById('loginPage').classList.add('hidden');
            document.getElementById('messagePage').classList.remove('hidden');
        });

        document.getElementById('envelopeButton').addEventListener('click', function() {
            document.getElementById('envelopeButton').classList.add('hidden');
            document.getElementById('messageContent').classList.remove('hidden');
        });

        document.getElementById('playButton').addEventListener('click', function() {
            document.getElementById('loveSong').play();
            document.getElementById('playButton').classList.remove('beat');
            document.getElementById('playButton').classList.add('break');
        });
    </script>
</body>
</html>
