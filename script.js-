/**
 * DB Normalization Lab - Funcionalidades Interativas
 * Arquivo: js/script.js
 */

document.addEventListener('DOMContentLoaded', () => {
    initCodeCopy();
    initScrollSpy();
    initReadingProgressBar();
    initSmoothScroll();
    initThemeToggle();
});

/**
 * 1. Botão de Copiar para Blocos de Código SQL
 */
function initCodeCopy() {
    const codeHeaders = document.querySelectorAll('.code-header');

    codeHeaders.forEach(header => {
        const copyBtn = document.createElement('button');
        copyBtn.className = 'btn-copy';
        copyBtn.innerText = 'Copiar SQL';
        copyBtn.setAttribute('aria-label', 'Copiar código SQL para a área de transferência');

        header.appendChild(copyBtn);

        copyBtn.addEventListener('click', async () => {
            const preBlock = header.nextElementSibling;
            if (!preBlock || preBlock.tagName !== 'PRE') return;

            const codeText = preBlock.innerText;

            try {
                await navigator.clipboard.writeText(codeText);
                copyBtn.innerText = 'Copiado!';
                copyBtn.classList.add('copied');

                setTimeout(() => {
                    copyBtn.innerText = 'Copiar SQL';
                    copyBtn.classList.remove('copied');
                }, 2000);
            } catch (err) {
                console.error('Erro ao copiar código:', err);
                copyBtn.innerText = 'Erro ao copiar';
            }
        });
    });
}

/**
 * 2. ScrollSpy: Destaca a secção visível no menu de navegação
 */
function initScrollSpy() {
    const sections = document.querySelectorAll('.section-block[id], .hero[id]');
    const navLinks = document.querySelectorAll('.main-nav a');

    if (!sections.length || !navLinks.length) return;

    const observerOptions = {
        root: null,
        rootMargin: '-20% 0px -60% 0px',
        threshold: 0
    };

    const observer = new IntersectionObserver((entries) => {
        entries.forEach(entry => {
            if (entry.isIntersecting) {
                const id = entry.target.getAttribute('id');
                if (!id) return;

                navLinks.forEach(link => {
                    link.classList.remove('active');
                    if (link.getAttribute('href') === `#${id}`) {
                        link.classList.add('active');
                    }
                });
            }
        });
    }, observerOptions);

    sections.forEach(section => observer.observe(section));
}

/**
 * 3. Indicador da Barra de Progresso de Leitura (com otimização requestAnimationFrame)
 */
function initReadingProgressBar() {
    const progressBar = document.createElement('div');
    progressBar.className = 'reading-progress-bar';
    document.body.appendChild(progressBar);

    let ticking = false;

    window.addEventListener('scroll', () => {
        if (!ticking) {
            window.requestAnimationFrame(() => {
                const winScroll = document.documentElement.scrollTop || document.body.scrollTop;
                const height = document.documentElement.scrollHeight - document.documentElement.clientHeight;
                const scrolled = height > 0 ? (winScroll / height) * 100 : 0;
                progressBar.style.width = `${scrolled}%`;
                ticking = false;
            });
            ticking = true;
        }
    });
}

/**
 * 4. Rolar Suave (Smooth Scroll) focado em Acessibilidade
 */
function initSmoothScroll() {
    const links = document.querySelectorAll('a[href^="#"]');

    links.forEach(link => {
        link.addEventListener('click', (e) => {
            const targetId = link.getAttribute('href');
            if (targetId === '#') return;

            const targetElement = document.querySelector(targetId);

            if (targetElement) {
                e.preventDefault();
                targetElement.scrollIntoView({
                    behavior: 'smooth',
                    block: 'start'
                });

                // Foco para leitores de ecrã
                targetElement.setAttribute('tabindex', '-1');
                targetElement.focus({ preventScroll: true });
            }
        });
    });
}

/**
 * 5. Alternador de Tema (Modo Claro / Escuro)
 */
function initThemeToggle() {
    const navContainer = document.querySelector('.main-header .container');
    if (!navContainer) return;

    const toggleBtn = document.createElement('button');
    toggleBtn.className = 'theme-toggle-btn';
    toggleBtn.setAttribute('aria-label', 'Alternar tema claro e escuro');
    toggleBtn.innerHTML = '🌙';

    navContainer.appendChild(toggleBtn);

    // Aplicar tema guardado no localStorage
    const savedTheme = localStorage.getItem('theme');
    if (savedTheme === 'dark') {
        document.documentElement.setAttribute('data-theme', 'dark');
        toggleBtn.innerHTML = '☀️';
    }

    toggleBtn.addEventListener('click', () => {
        const currentTheme = document.documentElement.getAttribute('data-theme');
        if (currentTheme === 'dark') {
            document.documentElement.removeAttribute('data-theme');
            localStorage.setItem('theme', 'light');
            toggleBtn.innerHTML = '🌙';
        } else {
            document.documentElement.setAttribute('data-theme', 'dark');
            localStorage.setItem('theme', 'dark');
            toggleBtn.innerHTML = '☀️';
        }
    });
}
