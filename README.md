# cpr_coffee-[index.html](https://github.com/user-attachments/files/33534112/index.html)
<!DOCTYPE html>
<html lang="fa" dir="rtl">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="theme-color" content="#39251d">
    <meta name="description" content="منوی نوشیدنی‌های CPR Café">
    <title>CPR Café | Coffee Menu</title>

    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link
        href="https://fonts.googleapis.com/css2?family=Vazirmatn:wght@400;500;600;700;800&family=Playfair+Display:wght@500;600;700&display=swap"
        rel="stylesheet">

    <style>
        :root {
            --espresso: #39251d;
            --coffee: #604331;
            --caramel: #a87950;
            --cream: #f8f1e7;
            --paper: #fffaf3;
            --muted: #88786b;
            --line: #e9dccd;
        }

        * {
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            margin: 0;
            background: var(--cream);
            color: var(--espresso);
            font-family: "Vazirmatn", sans-serif;
        }

        button {
            font: inherit;
        }

        .hero {
            position: relative;
            overflow: hidden;
            padding: 38px 20px 34px;
            text-align: center;
            color: var(--paper);
            background:
                linear-gradient(90deg, rgba(48, 32, 25, .92), rgba(48, 32, 25, .35)),
                url("images/hero.webp") center 52% / cover no-repeat,
                #39251d;
        }

        .hero::after {
            content: "";
            position: absolute;
            width: 180px;
            height: 180px;
            border: 1px solid rgba(232, 203, 164, .17);
            border-radius: 50%;
            top: -100px;
            left: -45px;
            box-shadow: 0 0 0 22px rgba(232, 203, 164, .035),
                0 0 0 44px rgba(232, 203, 164, .025);
            pointer-events: none;
        }

        .brand {
            position: relative;
            z-index: 1;
            margin: 0;
            font-family: "Playfair Display", serif;
            font-size: clamp(38px, 8vw, 58px);
            font-weight: 600;
            letter-spacing: 2px;
            direction: ltr;
        }

        .brand span {
            color: #d5ad81;
        }

        .subtitle {
            margin: 9px 0 0;
            color: #e9d8c6;
            font-size: 12px;
            letter-spacing: 4px;
            direction: ltr;
        }

        .hero-line {
            width: 44px;
            height: 2px;
            margin: 20px auto 14px;
            background: #c59b70;
        }

        .hero-caption {
            margin: 0;
            font-size: 13px;
            color: #f1e5d7;
        }

        main {
            width: min(100% - 28px, 980px);
            margin: 0 auto;
            padding: 26px 0 42px;
        }

        .intro {
            margin: 0 0 22px;
            text-align: center;
            color: var(--muted);
            font-size: 13px;
            line-height: 2;
        }

        .filters {
            display: flex;
            justify-content: center;
            gap: 8px;
            flex-wrap: wrap;
            margin-bottom: 28px;
        }

        .filter-btn {
            border: 1px solid #d9c7b4;
            border-radius: 999px;
            background: transparent;
            color: var(--coffee);
            padding: 8px 17px;
            font-size: 12px;
            cursor: pointer;
            transition: background .2s, color .2s;
        }

        .filter-btn:hover,
        .filter-btn.active {
            color: #fffaf3;
            background: var(--espresso);
            border-color: var(--espresso);
        }

        .menu-section {
            margin-bottom: 34px;
            scroll-margin-top: 20px;
        }

        .section-heading {
            display: flex;
            align-items: center;
            gap: 12px;
            margin: 0 0 17px;
        }

        .section-heading h2 {
            flex-shrink: 0;
            margin: 0;
            font-size: 19px;
            font-weight: 700;
        }

        .section-heading .en-heading {
            display: block;
            margin-top: 2px;
            color: var(--muted);
            font-family: "Playfair Display", serif;
            font-size: 12px;
            font-weight: 500;
            direction: ltr;
            text-align: right;
        }

        .section-heading::after {
            content: "";
            height: 1px;
            flex: 1;
            background: var(--line);
        }

        .menu-grid {
            display: grid;
            grid-template-columns: repeat(2, minmax(0, 1fr));
            gap: 13px;
        }

        .drink-card {
            display: flex;
            align-items: center;
            gap: 13px;
            min-width: 0;
            padding: 11px;
            background: var(--paper);
            border: 1px solid rgba(115, 78, 51, .09);
            border-radius: 15px;
            box-shadow: 0 4px 16px rgba(57, 37, 29, .035);
            transition: transform .2s, box-shadow .2s;
        }

        .drink-card:hover {
            transform: translateY(-2px);
            box-shadow: 0 7px 20px rgba(57, 37, 29, .08);
        }

        .drink-photo {
            display: block;
            flex: 0 0 84px;
            width: 84px;
            height: 84px;
            object-fit: cover;
            border-radius: 11px;
            background: #e9dccd;
        }

        .drink-info {
            min-width: 0;
            flex: 1;
        }

        .drink-fa {
            margin: 0;
            font-size: 14px;
            font-weight: 700;
            line-height: 1.9;
        }

        .drink-en {
            margin: 3px 0 0;
            color: var(--caramel);
            font-family: "Playfair Display", serif;
            font-size: 12px;
            font-weight: 600;
            direction: ltr;
            text-align: right;
            overflow-wrap: anywhere;
        }

        .contact-panel {
            margin: 28px 0 0;
            padding: 22px 18px;
            border: 1px solid #d9c2aa;
            border-radius: 18px;
            background: linear-gradient(135deg, #fffaf3, #f0e0cf);
            text-align: center;
            color: var(--coffee);
        }

        .pulse-heart {
            display: block;
            margin: 0 auto 12px;
            color: #8a4e3b;
            font-size: 30px;
            line-height: 1.2;
            letter-spacing: 3px;
        }

        .contact-line {
            margin: 9px 0;
            line-height: 1.9;
            font-size: 14px;
        }

        .contact-line a {
            color: var(--coffee);
            text-decoration: none;
            direction: ltr;
            display: inline-block;
        }

        .contact-line a:hover {
            text-decoration: underline;
        }

        .footer {
            padding: 25px 16px 28px;
            background: var(--espresso);
            color: #e9d8c6;
            text-align: center;
        }

        .footer-brand {
            margin: 0;
            font-family: "Playfair Display", serif;
            font-size: 22px;
            direction: ltr;
        }

        .footer-note {
            margin: 8px 0 0;
            color: #c8ae96;
            font-size: 11px;
        }

        .footer-slogan {
            margin: 15px 0 0;
            font-family: "Playfair Display", serif;
            font-size: 12px;
            direction: ltr;
            letter-spacing: .5px;
        }

        [hidden] {
            display: none !important;
        }

        @media (max-width: 540px) {
            .hero {
                padding: 32px 16px 29px;
            }

            main {
                width: calc(100% - 22px);
                padding-top: 22px;
            }

            .menu-grid {
                grid-template-columns: 1fr;
                gap: 10px;
            }

            .drink-card {
                padding: 10px;
            }

            .drink-photo {
                flex-basis: 78px;
                width: 78px;
                height: 78px;
            }

            .drink-fa {
                font-size: 14px;
            }

            .filter-btn {
                padding: 8px 13px;
            }
        }

        @media (prefers-reduced-motion: reduce) {

            *,
            *::before,
            *::after {
                scroll-behavior: auto !important;
                transition: none !important;
            }
        }
    </style>
</head>

<body>
    <header class="hero">
        <h1 class="brand">CPR <span>Café</span></h1>
        <p class="subtitle">COFFEE · TEA · MOMENTS</p>
        <div class="hero-line"></div>
        <p class="hero-caption">منوی نوشیدنی‌ها</p>
    </header>

    <main>
        <p class="intro">
            یه انتخاب خوش‌طعم برای لحظه‌های خوبت
        </p>

        <nav class="filters" aria-label="دسته‌بندی منو">
            <button class="filter-btn active" type="button" data-filter="all" aria-pressed="true">همه</button>
            <button class="filter-btn" type="button" data-filter="coffee" aria-pressed="false">قهوه گرم</button>
            <button class="filter-btn" type="button" data-filter="ice" aria-pressed="false">آیس</button>
            <button class="filter-btn" type="button" data-filter="tea" aria-pressed="false">چای</button>
            <button class="filter-btn" type="button" data-filter="herbal" aria-pressed="false">دمنوش</button>
            <button class="filter-btn" type="button" data-filter="other" aria-pressed="false">سایر نوشیدنی‌ها</button>
        </nav>

        <section class="menu-section" data-section="coffee">
            <div class="section-heading">
                <div>
                    <h2>قهوه گرم</h2>
                    <span class="en-heading">Hot Coffee</span>
                </div>
            </div>

            <div class="menu-grid">
                <article class="drink-card">
                    <img class="drink-photo" src="images/espresso.webp" alt="اسپرسو" loading="eager" decoding="async" fetchpriority="high" width="220" height="220">
                    <div class="drink-info">
                        <h3 class="drink-fa">اسپرسو</h3>
                        <p class="drink-en" lang="en">Espresso</p>
                    </div>
                </article>

                <article class="drink-card">
                    <img class="drink-photo" src="images/americano.webp" alt="آمریکانو" loading="eager" decoding="async" fetchpriority="high" width="220" height="220">
                    <div class="drink-info">
                        <h3 class="drink-fa">آمریکانو</h3>
                        <p class="drink-en" lang="en">Americano</p>
                    </div>
                </article>

                <article class="drink-card">
                    <img class="drink-photo" src="images/latte.webp" alt="لاته" loading="eager" decoding="async" fetchpriority="high" width="220" height="220">
                    <div class="drink-info">
                        <h3 class="drink-fa">لاته</h3>
                        <p class="drink-en" lang="en">Latte</p>
                    </div>
                </article>

                <article class="drink-card">
                    <img class="drink-photo" src="images/cappuccino.webp" alt="کاپوچینو" loading="eager" decoding="async" fetchpriority="high" width="220" height="220">
                    <div class="drink-info">
                        <h3 class="drink-fa">کاپوچینو</h3>
                        <p class="drink-en" lang="en">Cappuccino</p>
                    </div>
                </article>

                <article class="drink-card">
                    <img class="drink-photo" src="images/dirty-coffee.webp" alt="موکا" loading="eager" decoding="async" fetchpriority="high" width="220" height="220">
                    <div class="drink-info">
                        <h3 class="drink-fa">موکا</h3>
                        <p class="drink-en" lang="en">Mocha</p>
                    </div>
                </article>

                <article class="drink-card">
                    <img class="drink-photo" src="images/caramel-latte.webp" alt="کارامل ماکیاتو" loading="eager" decoding="async" fetchpriority="high" width="220" height="220">
                    <div class="drink-info">
                        <h3 class="drink-fa">کارامل ماکیاتو</h3>
                        <p class="drink-en" lang="en">Caramel Macchiato</p>
                    </div>
                </article>
            </div>
        </section>

        <section class="menu-section" data-section="ice">
            <div class="section-heading">
                <div>
                    <h2>نوشیدنی‌های آیس</h2>
                    <span class="en-heading">Iced Drinks</span>
                </div>
            </div>

            <div class="menu-grid">
                <article class="drink-card">
                    <img class="drink-photo" src="images/iced-americano.webp" alt="آیس آمریکانو" loading="eager" decoding="async" fetchpriority="high" width="220" height="220">
                    <div class="drink-info">
                        <h3 class="drink-fa">آیس آمریکانو</h3>
                        <p class="drink-en" lang="en">Iced Americano</p>
                    </div>
                </article>

                <article class="drink-card">
                    <img class="drink-photo" src="images/iced-latte.webp" alt="آیس لاته" loading="eager" decoding="async" fetchpriority="high" width="220" height="220">
                    <div class="drink-info">
                        <h3 class="drink-fa">آیس لاته</h3>
                        <p class="drink-en" lang="en">Iced Latte</p>
                    </div>
                </article>

                <article class="drink-card">
                    <img class="drink-photo" src="images/caramel-latte.webp" alt="آیس کارامل ماکیاتو" loading="eager" decoding="async" fetchpriority="high" width="220" height="220">
                    <div class="drink-info">
                        <h3 class="drink-fa">آیس کارامل ماکیاتو</h3>
                        <p class="drink-en" lang="en">Iced Caramel Macchiato</p>
                    </div>
                </article>

                <article class="drink-card">
                    <img class="drink-photo" src="images/cold-brew.webp" alt="آیس موکا" loading="eager" decoding="async" fetchpriority="high" width="220" height="220">
                    <div class="drink-info">
                        <h3 class="drink-fa">آیس موکا</h3>
                        <p class="drink-en" lang="en">Iced Mocha</p>
                    </div>
                </article>
            </div>
        </section>

        <section class="menu-section" data-section="tea">
            <div class="section-heading">
                <div>
                    <h2>چای</h2>
                    <span class="en-heading">Tea Selection</span>
                </div>
            </div>

            <div class="menu-grid">
                <article class="drink-card">
                    <img class="drink-photo" src="images/black-tea.webp" alt="چای سیاه" loading="eager" decoding="async" fetchpriority="high" width="220" height="220">
                    <div class="drink-info">
                        <h3 class="drink-fa">چای سیاه</h3>
                        <p class="drink-en" lang="en">Black Tea</p>
                    </div>
                </article>

                <article class="drink-card">
                    <img class="drink-photo" src="images/green-tea.webp" alt="چای سبز" loading="eager" decoding="async" fetchpriority="high" width="220" height="220">
                    <div class="drink-info">
                        <h3 class="drink-fa">چای سبز</h3>
                        <p class="drink-en" lang="en">Green Tea</p>
                    </div>
                </article>

                <article class="drink-card">
                    <img class="drink-photo" src="images/karak-chai.webp" alt="چای کرک" loading="eager" decoding="async" fetchpriority="high" width="220" height="220">
                    <div class="drink-info">
                        <h3 class="drink-fa">چای کرک</h3>
                        <p class="drink-en" lang="en">Karak Chai</p>
                    </div>
                </article>

                <article class="drink-card">
                    <img class="drink-photo" src="images/masala-chai.webp" alt="چای ماسالا" loading="eager" decoding="async" fetchpriority="high" width="220" height="220">
                    <div class="drink-info">
                        <h3 class="drink-fa">چای ماسالا</h3>
                        <p class="drink-en" lang="en">Masala Chai</p>
                    </div>
                </article>

                <article class="drink-card">
                    <img class="drink-photo" src="images/nabat-tea.webp" alt="چای نبات" loading="eager" decoding="async" width="220" height="220">
                    <div class="drink-info">
                        <h3 class="drink-fa">چای نبات</h3>
                        <p class="drink-en" lang="en">Tea with Rock Candy</p>
                    </div>
                </article>

                <article class="drink-card">
                    <img class="drink-photo" src="images/lemon-tea.webp" alt="چای به‌لیمو" loading="eager" decoding="async" width="220" height="220">
                    <div class="drink-info">
                        <h3 class="drink-fa">چای به‌لیمو</h3>
                        <p class="drink-en" lang="en">Lemon Verbena Tea</p>
                    </div>
                </article>
            </div>
        </section>

        <section class="menu-section" data-section="herbal">
            <div class="section-heading">
                <div>
                    <h2>دمنوش</h2>
                    <span class="en-heading">Herbal Infusions</span>
                </div>
            </div>

            <div class="menu-grid">
                <article class="drink-card">
                    <img class="drink-photo" src="images/herbal-tea.webp" alt="دمنوش گل گاوزبان" loading="eager" decoding="async" fetchpriority="high" width="220" height="220">
                    <div class="drink-info">
                        <h3 class="drink-fa">گل گاوزبان</h3>
                        <p class="drink-en" lang="en">Borage Herbal Tea</p>
                    </div>
                </article>
            </div>
        </section>

        <section class="menu-section" data-section="other">
            <div class="section-heading">
                <div>
                    <h2>سایر نوشیدنی‌ها</h2>
                    <span class="en-heading">More to Enjoy</span>
                </div>
            </div>

            <div class="menu-grid">

                <article class="drink-card">
                    <img class="drink-photo" src="images/lemonade.webp" alt="لیموناد" loading="eager" decoding="async" fetchpriority="high" width="220" height="220">
                    <div class="drink-info">
                        <h3 class="drink-fa">لیموناد</h3>
                        <p class="drink-en" lang="en">Lemonade</p>
                    </div>
                </article>

                <article class="drink-card">
                    <img class="drink-photo" src="images/mojito.webp" alt="موهیتو" loading="eager" decoding="async" fetchpriority="high" width="220" height="220">
                    <div class="drink-info">
                        <h3 class="drink-fa">موهیتو</h3>
                        <p class="drink-en" lang="en">Mojito</p>
                    </div>
                </article>

                <article class="drink-card">
                    <img class="drink-photo" src="images/dirty-coffee.webp" alt="هات چاکلت" loading="eager" decoding="async" fetchpriority="high" width="220" height="220">
                    <div class="drink-info">
                        <h3 class="drink-fa">هات چاکلت</h3>
                        <p class="drink-en" lang="en">Hot Chocolate</p>
                    </div>
                </article>

                <article class="drink-card">
                    <img class="drink-photo" src="images/pistachio-milk.webp" alt="شیر پسته" loading="eager" decoding="async" width="220" height="220">
                    <div class="drink-info">
                        <h3 class="drink-fa">شیر پسته</h3>
                        <p class="drink-en" lang="en">Pistachio Milk</p>
                    </div>
                </article>

                <article class="drink-card">
                    <img class="drink-photo" src="images/cocoa-milk.webp" alt="شیر کاکائو" loading="eager" decoding="async" width="220" height="220">
                    <div class="drink-info">
                        <h3 class="drink-fa">شیر کاکائو</h3>
                        <p class="drink-en" lang="en">Cocoa Milk</p>
                    </div>
                </article>
            </div>
        </section>
    </main>

    <section class="contact-panel" aria-label="اطلاعات تماس">
        <span class="pulse-heart" aria-label="ضربان قلب">〰️♥️〰️</span>
        <p class="contact-line">📍 روبروی سلف پردیس</p>
        <p class="contact-line">☎️ <a href="tel:09388152371">09388152371</a></p>
        <p class="contact-line">📷 <a href="https://instagram.com/cpr-coffe" target="_blank" rel="noopener noreferrer">@cpr-coffe</a></p>
    </section>

    <footer class="footer">
        <p class="footer-brand">CPR Café</p>
        <p class="footer-note">ممنون که انتخابمون کردی</p>
        <p class="footer-slogan">Make a good time for good thing</p>
    </footer>

    <script>
        "use strict";

        const filterButtons = document.querySelectorAll(".filter-btn");
        const menuSections = document.querySelectorAll(".menu-section");

        filterButtons.forEach((button) => {
            button.addEventListener("click", () => {
                const selectedFilter = button.dataset.filter;

                filterButtons.forEach((item) => {
                    const isActive = item === button;
                    item.classList.toggle("active", isActive);
                    item.setAttribute("aria-pressed", String(isActive));
                });

                menuSections.forEach((section) => {
                    section.hidden =
                        selectedFilter !== "all" &&
                        section.dataset.section !== selectedFilter;
                });
            });
        });
    </script>
</body>

</html>
