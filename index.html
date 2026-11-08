<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DimaPay Helper</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        .editable:focus { outline: 2px dashed #ff8562; background-color: rgba(255, 133, 98, 0.05); }
        .dimapay-watermark {
            position: fixed; bottom: 20px; right: 20px; z-index: 9999;
            background: rgba(15, 23, 42, 0.9); backdrop-filter: blur(8px);
            border: 1px solid rgba(255, 255, 255, 0.15); box-shadow: 0 10px 25px -5px rgba(0, 0, 0, 0.3);
        }
    </style>
</head>
<body class="bg-gray-100 font-sans text-gray-800 antialiased min-h-screen flex flex-col">

    <!-- ЭКРАН ВХОДА -->
    <div id="loginScreen" class="fixed inset-0 bg-slate-900 z-50 flex items-center justify-center p-4">
        <div class="bg-white rounded-2xl shadow-2xl max-w-md w-full p-8 border border-slate-700/50">
            <div class="text-center mb-8">
                <div class="inline-flex items-center space-x-2 mb-3">
                    <span class="bg-gradient-to-r from-orange-500 to-amber-500 text-white font-black px-3 py-1.5 rounded-lg text-xl">DP</span>
                    <span class="font-bold text-2xl text-slate-800">DimaPay <span class="text-orange-500">Helper</span></span>
                </div>
                <p class="text-sm text-gray-500">Введите логин и пароль для доступа к конструктору</p>
            </div>

            <form onsubmit="handleLogin(event)" class="space-y-5">
                <div>
                    <label class="block text-xs font-bold text-gray-600 uppercase mb-1.5">Логин</label>
                    <div class="relative">
                        <i class="fa-solid fa-user absolute left-3.5 top-3.5 text-gray-400 text-sm"></i>
                        <input type="text" id="loginUser" value="admin" class="w-full border border-gray-300 rounded-lg pl-10 pr-4 py-2.5 text-sm focus:ring-2 focus:ring-orange-500 focus:border-orange-500 outline-none" placeholder="Логин" required>
                    </div>
                </div>

                <div>
                    <label class="block text-xs font-bold text-gray-600 uppercase mb-1.5">Пароль</label>
                    <div class="relative">
                        <i class="fa-solid fa-lock absolute left-3.5 top-3.5 text-gray-400 text-sm"></i>
                        <input type="password" id="loginPass" value="dimaDurov12@" class="w-full border border-gray-300 rounded-lg pl-10 pr-4 py-2.5 text-sm focus:ring-2 focus:ring-orange-500 focus:border-orange-500 outline-none" placeholder="Пароль" required>
                    </div>
                </div>

                <div id="loginError" class="text-red-500 text-xs font-medium hidden text-center">Неверный логин или пароль</div>

                <button type="submit" class="w-full bg-orange-500 hover:bg-orange-600 text-white font-bold py-3 rounded-lg text-sm transition shadow-lg shadow-orange-500/30">
                    Войти в систему
                </button>
            </form>
        </div>
    </div>

    <!-- ОСНОВНОЙ ИНТЕРФЕЙС КОНСТРУКТОРА -->
    <div id="appScreen" class="hidden flex-col min-h-screen">
        <header class="bg-slate-900 text-white h-16 flex items-center justify-between px-6 shadow-md sticky top-0 z-40">
            <div class="flex items-center space-x-4">
                <div class="flex items-center space-x-2">
                    <span class="bg-gradient-to-r from-orange-500 to-amber-500 text-white font-black px-2.5 py-1 rounded text-lg tracking-wider">DP</span>
                    <span class="font-bold text-lg tracking-tight">DimaPay <span class="text-orange-400">Helper</span></span>
                </div>
                <span class="bg-emerald-500/20 text-emerald-400 text-xs px-2.5 py-1 rounded-full border border-emerald-500/30 font-medium flex items-center gap-1">
                    <i class="fa-solid fa-crown text-amber-400"></i> Премиум Тариф
                </span>
            </div>

            <div class="flex items-center space-x-3">
                <button onclick="openModal('userMgmtModal')" class="bg-blue-600 hover:bg-blue-500 text-white text-xs font-semibold px-3 py-2 rounded flex items-center gap-1.5 transition">
                    <i class="fa-solid fa-users-gear"></i> Пользователи (Админка)
                </button>
                <button onclick="openModal('wpModal')" class="bg-gray-700 hover:bg-gray-600 text-xs font-semibold px-3 py-2 rounded flex items-center gap-1.5 transition">
                    <i class="fa-brands fa-wordpress text-blue-400"></i> База Данных WP
                </button>
                <button onclick="openModal('widgetModal')" class="bg-gray-700 hover:bg-gray-600 text-xs font-semibold px-3 py-2 rounded flex items-center gap-1.5 transition">
                    <i class="fa-solid fa-code text-amber-400"></i> Код Виджета
                </button>
                <button onclick="exportHTML()" class="bg-orange-500 hover:bg-orange-600 text-white text-xs font-semibold px-4 py-2 rounded flex items-center gap-1.5 transition shadow">
                    <i class="fa-solid fa-download"></i> Скачать HTML
                </button>
                <div class="h-6 w-px bg-gray-700 mx-1"></div>
                <button onclick="logout()" class="bg-red-600/80 hover:bg-red-600 text-white text-xs font-semibold px-3 py-2 rounded transition">
                    <i class="fa-solid fa-right-from-bracket"></i> Выход
                </button>
            </div>
        </header>

        <div class="flex flex-1 overflow-hidden">
            <aside class="w-72 bg-white border-r border-gray-200 p-4 flex flex-col gap-4 overflow-y-auto">
                <h3 class="text-xs font-bold text-gray-400 uppercase tracking-wider mb-3">Добавить блоки</h3>
                <div class="space-y-2">
                    <button onclick="addBlock('hero')" class="w-full text-left p-3 border border-gray-200 rounded-lg hover:border-orange-500 transition bg-white font-semibold text-sm">
                        <i class="fa-solid fa-desktop mr-2 text-gray-400"></i>Главная обложка
                    </button>
                    <button onclick="addBlock('authWidget')" class="w-full text-left p-3 border border-gray-200 rounded-lg hover:border-orange-500 transition bg-white font-semibold text-sm">
                        <i class="fa-solid fa-right-to-bracket mr-2 text-gray-400"></i>Форма Авторизации
                    </button>
                    <button onclick="addBlock('tariffs')" class="w-full text-left p-3 border border-gray-200 rounded-lg hover:border-orange-500 transition bg-white font-semibold text-sm">
                        <i class="fa-solid fa-tags mr-2 text-gray-400"></i>Тарифные планы
                    </button>
                    <button onclick="addBlock('payment')" class="w-full text-left p-3 border border-gray-200 rounded-lg hover:border-orange-500 transition bg-white font-semibold text-sm">
                        <i class="fa-solid fa-credit-card mr-2 text-gray-400"></i>Оплата DimaPay
                    </button>
                    <button onclick="addBlock('footer')" class="w-full text-left p-3 border border-gray-200 rounded-lg hover:border-orange-500 transition bg-white font-semibold text-sm">
                        <i class="fa-solid fa-bullhorn mr-2 text-gray-400"></i>Подвал сайта
                    </button>
                </div>
            </aside>

            <main class="flex-1 overflow-y-auto p-8 bg-gray-200 flex justify-center">
                <div id="canvas" class="w-full max-w-4xl bg-white shadow-xl min-h-[800px] relative">
                    <div class="block-wrapper group relative border border-transparent hover:border-orange-500 transition-all">
                        <div class="absolute right-3 top-3 hidden group-hover:flex items-center gap-1 bg-white border p-1 rounded shadow-md z-30">
                            <button onclick="moveUp(this)" class="p-1 text-gray-600"><i class="fa-solid fa-arrow-up"></i></button>
                            <button onclick="moveDown(this)" class="p-1 text-gray-600"><i class="fa-solid fa-arrow-down"></i></button>
                            <button onclick="removeBlock(this)" class="p-1 text-red-600"><i class="fa-solid fa-trash"></i></button>
                        </div>
                        <section class="py-20 px-8 text-center bg-gradient-to-b from-slate-900 to-slate-800 text-white">
                            <h1 class="editable text-4xl md:text-5xl font-extrabold mb-4" contenteditable="true">Создавайте сайты с DimaPay Helper</h1>
                            <p class="editable text-lg text-slate-300 max-w-2xl mx-auto mb-8" contenteditable="true">Конструктор лендингов, виджетов авторизации и платежных модулей.</p>
                            <button class="editable bg-orange-500 hover:bg-orange-600 text-white px-8 py-3.5 rounded-lg font-bold transition shadow-lg" contenteditable="true">Начать работу</button>
                        </section>
                    </div>
                </div>
            </main>
        </div>
    </div>

    <!-- УПРАВЛЕНИЕ ПОЛЬЗОВАТЕЛЯМИ (АДМИНКА) -->
    <div id="userMgmtModal" class="fixed inset-0 bg-black/60 backdrop-blur-sm z-50 hidden flex items-center justify-center p-4">
        <div class="bg-white rounded-xl shadow-2xl max-w-2xl w-full p-6 relative">
            <button onclick="closeModal('userMgmtModal')" class="absolute top-4 right-4 text-gray-400 hover:text-gray-600"><i class="fa-solid fa-xmark text-lg"></i></button>
            <h3 class="text-xl font-bold mb-4 flex items-center gap-2"><i class="fa-solid fa-users-gear text-blue-600"></i> Создание и управление пользователями</h3>

            <form onsubmit="createUser(event)" class="bg-gray-50 p-4 rounded-lg border border-gray-200 mb-6 space-y-3">
                <div class="font-semibold text-xs text-gray-500 uppercase">Добавить нового пользователя</div>
                <div class="grid grid-cols-3 gap-3">
                    <input type="text" id="newUsername" placeholder="Логин" class="border rounded px-3 py-2 text-sm outline-none" required>
                    <input type="password" id="newPassword" placeholder="Пароль" class="border rounded px-3 py-2 text-sm outline-none" required>
                    <select id="newRole" class="border rounded px-3 py-2 text-sm outline-none">
                        <option value="Пользователь">Пользователь</option>
                        <option value="Администратор">Администратор</option>
                    </select>
                </div>
                <button type="submit" class="bg-blue-600 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded text-xs transition">Создать пользователя</button>
            </form>

            <div class="font-semibold text-xs text-gray-500 uppercase mb-2">Зарегистрированные аккаунты</div>
            <div class="border rounded-lg overflow-hidden">
                <table class="w-full text-left text-xs">
                    <thead class="bg-gray-100 text-gray-600 border-b">
                        <tr>
                            <th class="p-3">Логин</th>
                            <th class="p-3">Роль</th>
                            <th class="p-3 text-right">Действие</th>
                        </tr>
                    </thead>
                    <tbody id="userTableBody" class="divide-y"></tbody>
                </table>
            </div>
        </div>
    </div>

    <!-- WORDPRESS & БД -->
    <div id="wpModal" class="fixed inset-0 bg-black/60 backdrop-blur-sm z-50 hidden flex items-center justify-center p-4">
        <div class="bg-white rounded-xl shadow-2xl max-w-lg w-full p-6 relative">
            <button onclick="closeModal('wpModal')" class="absolute top-4 right-4 text-gray-400 hover:text-gray-600"><i class="fa-solid fa-xmark text-lg"></i></button>
            <h3 class="text-xl font-bold mb-4 flex items-center gap-2"><i class="fa-brands fa-wordpress text-blue-500"></i> Настройка базы данных WordPress</h3>
            <form onsubmit="alert('База данных успешно подключена!'); closeModal('wpModal');" class="space-y-4">
                <div>
                    <label class="block text-xs font-bold text-gray-600 uppercase mb-1">Адрес REST API</label>
                    <input type="url" value="https://dimapayconstructor.wordpress.com/wp-json" class="w-full border rounded px-3 py-2 text-sm outline-none">
                </div>
                <div class="grid grid-cols-2 gap-3">
                    <div>
                        <label class="block text-xs font-bold text-gray-600 uppercase mb-1">Хост MySQL</label>
                        <input type="text" value="localhost" class="w-full border rounded px-3 py-2 text-sm outline-none">
                    </div>
                    <div>
                        <label class="block text-xs font-bold text-gray-600 uppercase mb-1">Имя БД</label>
                        <input type="text" value="wp_dimapay" class="w-full border rounded px-3 py-2 text-sm outline-none">
                    </div>
                </div>
                <button type="submit" class="w-full bg-emerald-600 hover:bg-emerald-700 text-white font-bold py-2.5 rounded transition text-sm">Сохранить</button>
            </form>
        </div>
    </div>

    <!-- МОДАЛЬНОЕ ОКНО: ВИДЖЕТ -->
    <div id="widgetModal" class="fixed inset-0 bg-black/60 backdrop-blur-sm z-50 hidden flex items-center justify-center p-4">
        <div class="bg-white rounded-xl shadow-2xl max-w-xl w-full p-6 relative">
            <button onclick="closeModal('widgetModal')" class="absolute top-4 right-4 text-gray-400 hover:text-gray-600"><i class="fa-solid fa-xmark text-lg"></i></button>
            <h3 class="text-xl font-bold mb-2 flex items-center gap-2"><i class="fa-solid fa-code text-amber-500"></i> Код виджета</h3>
            <textarea readonly class="w-full h-32 font-mono text-xs p-3 bg-slate-900 text-slate-200 rounded border">&lt;script src="https://dimapay.helper.tilda.ws/widget.js"&gt;&lt;/script&gt;</textarea>
            <button onclick="navigator.clipboard.writeText(document.querySelector('#widgetModal textarea').value); alert('Код скопирован!');" class="mt-3 w-full bg-slate-800 text-white font-bold py-2 rounded text-xs">Скопировать</button>
        </div>
    </div>

    <!-- ВОДЯНОЙ ЗНАК -->
    <div class="dimapay-watermark px-4 py-2.5 rounded-full flex items-center space-x-3 text-white text-xs font-semibold">
        <div class="w-2.5 h-2.5 rounded-full bg-emerald-400 animate-pulse"></div>
        <span class="text-slate-300">Работает на <strong class="text-white font-bold">DimaPay Helper</strong></span>
    </div>

    <script>
        let usersList = [{ login: 'admin', pass: 'dimaDurov12@', role: 'Администратор' }];

        function handleLogin(e) {
            e.preventDefault();
            const loginInput = document.getElementById('loginUser').value;
            const passInput = document.getElementById('loginPass').value;
            const errDiv = document.getElementById('loginError');
            const foundUser = usersList.find(u => u.login === loginInput && u.pass === passInput);

            if (foundUser) {
                errDiv.classList.add('hidden');
                document.getElementById('loginScreen').classList.add('hidden');
                document.getElementById('appScreen').classList.remove('hidden');
                document.getElementById('appScreen').classList.add('flex');
                renderUserTable();
            } else {
                errDiv.classList.remove('hidden');
            }
        }

        function logout() {
            document.getElementById('appScreen').classList.add('hidden');
            document.getElementById('appScreen').classList.remove('flex');
            document.getElementById('loginScreen').classList.remove('hidden');
        }

        function renderUserTable() {
            const tbody = document.getElementById('userTableBody');
            if(!tbody) return;
            tbody.innerHTML = '';
            usersList.forEach((u, index) => {
                const tr = document.createElement('tr');
                tr.className = "hover:bg-gray-50";
                tr.innerHTML = `
                    <td class="p-3 font-medium text-gray-800">${u.login}</td>
                    <td class="p-3"><span class="px-2 py-0.5 text-[10px] font-bold rounded ${u.role === 'Администратор' ? 'bg-purple-100 text-purple-700' : 'bg-gray-100 text-gray-600'}">${u.role}</span></td>
                    <td class="p-3 text-right">
                        ${index !== 0 ? `<button onclick="deleteUser(${index})" class="text-red-500 hover:text-red-700 font-semibold">Удалить</button>` : '<span class="text-gray-400">Главный</span>'}
                    </td>
                `;
                tbody.appendChild(tr);
            });
        }

        function createUser(e) {
            e.preventDefault();
            const login = document.getElementById('newUsername').value;
            const pass = document.getElementById('newPassword').value;
            const role = document.getElementById('newRole').value;
            usersList.push({ login, pass, role });
            document.getElementById('newUsername').value = '';
            document.getElementById('newPassword').value = '';
            renderUserTable();
            alert(`Пользователь ${login} успешно создан!`);
        }

        function deleteUser(index) {
            usersList.splice(index, 1);
            renderUserTable();
        }

        function openModal(id) { document.getElementById(id).classList.remove('hidden'); }
        function closeModal(id) { document.getElementById(id).classList.add('hidden'); }

        const templates = {
            hero: `<section class="py-20 px-8 text-center bg-gradient-to-b from-slate-900 to-slate-800 text-white"><h1 class="editable text-4xl md:text-5xl font-extrabold mb-4" contenteditable="true">Заголовок</h1><p class="editable text-lg text-slate-300 max-w-2xl mx-auto mb-8" contenteditable="true">Описание</p></section>`,
            authWidget: `<section class="py-12 px-6 bg-slate-50 flex justify-center"><div class="max-w-md w-full bg-white p-6 rounded-xl shadow-lg"><h2 class="editable text-xl font-bold text-center mb-4" contenteditable="true">Авторизация</h2><input type="text" placeholder="Логин" class="w-full border mb-3 p-2 rounded"><input type="password" placeholder="Пароль" class="w-full border mb-3 p-2 rounded"><button class="w-full bg-slate-900 text-white py-2 rounded">Войти</button></div></section>`,
            tariffs: `<section class="py-12 px-6 bg-white"><h2 class="editable text-2xl font-bold text-center mb-6" contenteditable="true">Тарифы</h2><div class="grid grid-cols-2 gap-4"><div class="border p-4 rounded text-center"><h3 class="font-bold">Базовый</h3><p>0 ₽</p></div><div class="border p-4 rounded text-center bg-orange-50"><h3 class="font-bold text-orange-500">PRO</h3><p>990 ₽</p></div></div></section>`,
            payment: `<section class="py-8 px-6 bg-slate-900 text-white text-center"><h3 class="font-bold text-lg mb-2">Оплата DimaPay</h3><button class="bg-emerald-500 text-white px-6 py-2 rounded font-bold">Оплатить 1000 ₽</button></section>`,
            footer: `<footer class="py-6 px-4 bg-slate-900 text-gray-400 text-xs text-center"><p>© 2026 DimaPay Helper</p></footer>`
        };

        function addBlock(type) {
            const canvas = document.getElementById('canvas');
            const wrapper = document.createElement('div');
            wrapper.className = 'block-wrapper group relative border border-transparent hover:border-orange-500 transition-all';
            wrapper.innerHTML = `
                <div class="absolute right-3 top-3 hidden group-hover:flex items-center gap-1 bg-white border p-1 rounded shadow-md z-30">
                    <button onclick="moveUp(this)" class="p-1 text-gray-600"><i class="fa-solid fa-arrow-up"></i></button>
                    <button onclick="moveDown(this)" class="p-1 text-gray-600"><i class="fa-solid fa-arrow-down"></i></button>
                    <button onclick="removeBlock(this)" class="p-1 text-red-600"><i class="fa-solid fa-trash"></i></button>
                </div>
                ${templates[type]}
            `;
            canvas.appendChild(wrapper);
        }

        function moveUp(btn) { const b = btn.closest('.block-wrapper'); if(b.previousElementSibling) b.parentNode.insertBefore(b, b.previousElementSibling); }
        function moveDown(btn) { const b = btn.closest('.block-wrapper'); if(b.nextElementSibling) b.parentNode.insertBefore(b.nextElementSibling, b); }
        function removeBlock(btn) { btn.closest('.block-wrapper').remove(); }

        function exportHTML() {
            const clone = document.getElementById('canvas').cloneNode(true);
            clone.querySelectorAll('.absolute').forEach(e => e.remove());
            clone.querySelectorAll('[contenteditable]').forEach(e => e.removeAttribute('contenteditable'));
            const blob = new Blob([clone.innerHTML], { type: 'text/html' });
            const a = document.createElement('a');
            a.href = URL.createObjectURL(blob);
            a.download = 'dimapay-landing.html';
            a.click();
        }
    </script>
</body>
</html>
