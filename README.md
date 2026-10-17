(https://github.com/user-attachments/files/33601520/README.3.md)
<div align="center">

# ✓ AttendX

**Know your attendance before your attendance sheet does.**

![Single File](https://img.shields.io/badge/SINGLE%20FILE-0C1D3D?style=for-the-badge)
![Zero Dependencies](https://img.shields.io/badge/ZERO%20DEPENDENCIES-356FF5?style=for-the-badge)
![Offline First](https://img.shields.io/badge/OFFLINE%20FIRST-6947F5?style=for-the-badge)
![75% Alerts](https://img.shields.io/badge/75%25%20ALERTS-F05262?style=for-the-badge)

[Live Demo](https://YOUR-USERNAME.github.io/attendx) · [Report an Issue](../../issues)

</div>

---

## 🧾 At a Glance

| | |
|---|---|
| **What it is** | A student attendance tracker that runs in one HTML file |
| **Who it's for** | Students who need to stay above the 75% line |
| **Pages** | 8 (Dashboard, Attendance, Subjects, Calendar, Analytics, Reports, Profile, Settings) |
| **Storage** | Your browser's `localStorage`, nothing leaves your device |
| **Install** | None. Open `index.html` |
| **Stack** | HTML, CSS, vanilla JavaScript |

## ⏱️ Try It in 30 Seconds

1. Open `index.html`. Demo data for six subjects is already loaded.
2. Go to **Attendance**, pick a subject, choose **Present**, **Absent** or **Late**, and save.
3. Watch the dashboard, subject bars and calendar dots update instantly.
4. Open **Settings → Reset demo data** whenever you want a clean start.

## 🖥️ The Eight Screens

| Screen | What you get |
|---|---|
| 🏠 **Dashboard** | Overall percentage, present / absent / late counts, subject performance, mini calendar, recent records, quick actions |
| ✅ **Attendance** | Log a class by subject, date, status and optional note, plus the full record table |
| 📚 **Subjects** | One card per subject with percentage, present and absent counts. Green at 75% and above, red below |
| 📅 **Calendar** | Current month with coloured dots: 🟢 present, 🟠 late, 🔴 absent |
| 📈 **Analytics** | Overall, highest and lowest attendance, total classes and a subject comparison chart |
| 🖨️ **Reports** | A clean printable report with every record and your overall percentage |
| 👤 **Profile** | Your name, course and year, shown across the app |
| ⚙️ **Settings** | Dark mode toggle and demo data reset |

Also included: a search box that filters the subject list, toast notifications, and a sidebar that collapses to icons on small screens.

## 🧮 The Maths

```text
Subject %  = present ÷ total classes × 100
Overall %  = Σ present ÷ Σ total × 100
```

- Only **Present** counts as attended. **Late** and **Absent** both count against you.
- Any subject below **75%** appears in the **Low Attendance Alert** on the dashboard.
- Saving a second entry for the same subject and date updates that record instead of creating a duplicate.

## 🧱 Data Model

Everything lives in a single object saved under the key `attendx-v1`:

```json
{
  "profile":  { "name": "", "course": "", "year": "" },
  "subjects": [ { "name": "Java", "total": 32, "present": 29 } ],
  "records":  [ { "date": "2026-09-18", "subject": "Java", "status": "Present", "notes": "" } ]
}
```

Because it is plain JSON, backing it up is as easy as copying the value from your browser's DevTools (**Application → Local Storage**).

## 🗂️ App Layout

```text
┌──────────┬───────────────────────────────────────────┐
│ AttendX  │  🔍 Search            ☾  ♧   👤 Profile   │
│          ├───────────────────────────────────────────┤
│ Dashboard│   Overall   Present   Absent   Late       │
│ Attend…  │   ┌──────────────┐ ┌──────────┐ ┌───────┐ │
│ Subjects │   │ Overview     │ │ Subjects │ │ Calen │ │
│ Calendar │   └──────────────┘ └──────────┘ └───────┘ │
│ Analytics│   ┌──────────────────────┐ ┌────────────┐ │
│ Reports  │   │ Recent attendance    │ │ Quick acts │ │
│ Profile  │   └──────────────────────┘ └────────────┘ │
│ Settings │                                           │
└──────────┴───────────────────────────────────────────┘
```

## 🚀 Run It

```bash
git clone https://github.com/YOUR-USERNAME/attendx.git
cd attendx
open index.html        # or: npx serve .
```

**Deploy free:** GitHub Pages (Settings → Pages → `main`), Netlify drag and drop, or Vercel import.

## 🎨 Make It Yours

```css
:root{
  --primary:#356ff5;   /* main blue */
  --primary2:#6947f5;  /* gradient partner */
  --green:#19b77a;     /* 75% and above */
  --red:#f05262;       /* below 75% */
}
```

To change the demo subjects, edit the `defaultData` object near the top of the script.

## ❓ FAQ

<details>
<summary><b>Is my data uploaded anywhere?</b></summary>

No. AttendX has no server. Your records stay in your browser, so clearing site data will erase them.
</details>

<details>
<summary><b>Can I use it on my phone?</b></summary>

Yes. The layout is responsive and the sidebar shrinks to an icon rail on narrow screens.
</details>

<details>
<summary><b>Why is Late not counted as present?</b></summary>

Many institutions mark late arrivals as absent for the hour. If yours does not, change the condition in `saveAttendance()` so Late also increases `present`.
</details>

## 🗺️ Roadmap

- [x] Subjects, records, calendar, analytics and printable report
- [x] 75% low-attendance alerts
- [x] Persistent storage
- [ ] "Classes I can still skip" calculator per subject
- [ ] Working 7 day / 30 day / 3 month chart ranges
- [ ] Fix recalculation when editing an existing record's status
- [ ] Persistent dark mode
- [ ] Import and export data as JSON or CSV
- [ ] Timetable-based reminders

## 🤝 Contributing

Fork, branch, commit, and open a pull request. Small, focused changes are the easiest to review.

## 👨‍💻 Author

**S.S. Manikanda Prabu**, B.Tech CSE, SRM Institute of Science and Technology, Ramapuram

[GitHub](https://github.com/YOUR-USERNAME) · [LinkedIn](https://linkedin.com/in/YOUR-PROFILE)

<div align="center">

<sub>Built so you never have to guess your percentage again. ⭐ if it helped.</sub>

</div>
