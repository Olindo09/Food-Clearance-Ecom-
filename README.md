# 🍽️ Food Clearance – Save Food, Save Money, Save the Planet 🌍

## The Story Behind the Project
Every day, tons of perfectly edible food goes to waste simply because it’s close to its expiry date. Grocery stores and restaurants often struggle to manage this inventory, while people in the community are searching for affordable meals.  

**Food Clearance** was born from that challenge:  
👉 A platform where businesses can upload their soon-to-expire food,  
👉 Customers can discover discounts, and  
👉 Admins can oversee the entire ecosystem to make sure it’s fair and transparent.  

It’s more than just software — it’s an effort to **reduce waste, cut costs, and make food accessible**.

---

## 🚀 Features
- **Customers**: browse discounted food, search by expiry/category, add to cart  
- **Companies**: upload food items, manage inventory, track transactions  
- **Admins**: manage users, foods, companies, transactions, reports  
- **Reports**: track expired vs sold items, generate audits  

---

## 🏗️ Project Structure
food-clearance/  
├─ app/                # Controllers, Models, Middleware  
├─ bootstrap/          # Laravel bootstrap files  
├─ config/             # Configuration (auth, DB, mail, etc.)  
├─ database/           # Migrations & Seeders  
├─ public/             # Frontend entry (index.php, assets)  
├─ resources/          # Views (Blade templates), JS, CSS  
├─ routes/             # Web & API routes  
├─ storage/            # Logs, cache, uploads  
├─ tests/              # PHPUnit tests  
├─ artisan             # Laravel CLI  
├─ composer.json       # PHP dependencies  
├─ package.json        # JS dependencies  
└─ .env.example        # Example environment variables  

---

## 📌 Key Routes
- `/` → Home page  
- `/home` → Authenticated landing  
- **Admin**: `/admin/users`, `/admin/foods`, `/admin/companies`, `/admin/transactions`, `/admin/reports`  
- **Company**: `/company/foods`, `/company/transactions`, `/company/companies`  
- **Customer**: `/cart`, `/search`  

---

## 🛠️ Tech Stack
- **Backend**: Laravel (PHP 8+)  
- **Frontend**: Blade, Bootstrap, Mix (Webpack)  
- **Database**: MySQL  
- **Auth**: Multi-role (Admin, Company, Customer)  
- **Testing**: PHPUnit  
- **Packages**: Composer, NPM  

---

## 🧑‍💻 SQL & Data Skills Showcase
- **Schema Design**: Users, Foods, Companies, Transactions, Reports  
- **Joins & Queries**: insights on discounts, sales, waste  
- **Stored Procedures / Views**: reusable logic for reporting  
- **Transaction Logs**: ensure atomic sales  

Example SQL:  
SELECT c.name AS company_name,  
       COUNT(CASE WHEN f.status = 'expired' THEN 1 END) * 100.0 / COUNT(*) AS expired_pct  
FROM foods f  
JOIN companies c ON f.company_id = c.id  
GROUP BY c.name;  

---

## 🏭 ETL, Warehousing & Analytics
- **ETL**: extract sales data, transform discounts/expiry, load into warehouse  
- **Warehouse**: fact (transactions), dimensions (company, food, time, location)  
- **Analytics**: dashboards for saved vs wasted food, revenue recovery, adoption rate  
- **Predictive**: forecast unsold categories, recommend discounts by expiry  

---

## ⚙️ Installation
git clone https://github.com/<your-username>/food-clearance-ecom-.git  
cd food-clearance-ecom-  
composer install  
npm install && npm run dev  
cp .env.example .env  
php artisan key:generate  
php artisan migrate --seed  
php artisan serve  

Visit: http://localhost:8000  

---

## 🎯 Usage Flow
1. Admin sets up companies  
2. Companies upload expiring food  
3. Customers browse & buy  
4. Transactions logged → Reports generated  
5. ETL → Warehouse → Analytics dashboards  

---

## 🌱 Roadmap
- Mobile app (Flutter/React Native)  
- AI-powered discount engine  
- Notifications for new deals  
- Multi-language & multi-currency  
- Delivery service integration  
- Automated pipelines (Airflow/dbt)  

---

## ❤️ Mission
This project isn’t just about code — it’s about impact.  
By making food redistribution efficient and accessible, **we aim to cut waste, feed more people, and support businesses.**  

*"Save food, save money, save the planet."* 🌍✨
