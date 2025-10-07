/*
Portfolio React component (single-file)
Tech: React + TailwindCSS + Framer Motion
How to use:
1. Create a new React app (Vite recommended) and add TailwindCSS and Framer Motion.
2. Drop this file as `src/Portfolio.jsx` and import it in `App.jsx`.
3. Replace placeholder project details and links with your real ones.
4. Commit to a GitHub repo with a README (example README template included below).

Suggested repo structure:
- / (repo root)
  - README.md
  - package.json
  - tailwind.config.js
  - postcss.config.js
  - /src
    - main.jsx
    - App.jsx
    - Portfolio.jsx  <-- this file
    - index.css
  - /public

README template (brief):
# M Zahoor — Software Developer (Flutter & Web)
- Email: mzahoor575@gmail.com
- Phone: +92 3365884687
- Education: BSc Computer Science
- Experience: 1+ year in Flutter
- Projects: 12+ (see /projects or Portfolio.jsx)

## Run locally
1. npm install
2. npm run dev

---
*/

import React from 'react'
import { motion } from 'framer-motion'

const projects = [
  { id: 1, title: 'Project One', desc: 'A short description of project one. Built with Flutter + Firebase.', tech: ['Flutter','Firebase'], github:'#', demo:'#' },
  { id: 2, title: 'Project Two', desc: 'Cross-platform mobile app for X. Includes auth and push notifications.', tech: ['Flutter','REST API'], github:'#', demo:'#' },
  { id: 3, title: 'E-Commerce App', desc: 'End-to-end shopping app with payment integration.', tech: ['Flutter','Stripe'], github:'#', demo:'#' },
  { id: 4, title: 'Portfolio CMS', desc: 'Headless CMS for portfolio content management.', tech: ['React','GraphQL'], github:'#', demo:'#' },
  { id: 5, title: 'Chat App', desc: 'Real-time chat with WebSockets and presence.', tech: ['Flutter','Socket.IO'], github:'#', demo:'#' },
  { id: 6, title: 'Task Manager', desc: 'Productivity app with offline sync.', tech: ['Flutter','SQLite'], github:'#', demo:'#' },
  { id: 7, title: 'Travel Guide', desc: 'Location-based travel guide app with maps.', tech: ['Flutter','Google Maps'], github:'#', demo:'#' },
  { id: 8, title: 'FinTrack', desc: 'Personal finance tracker with charts.', tech: ['Flutter','Dart'], github:'#', demo:'#' },
  { id: 9, title: 'News Reader', desc: 'Aggregates news from multiple sources.', tech: ['Flutter','RSS'], github:'#', demo:'#' },
  { id: 10, title: 'IoT Dashboard', desc: 'Dashboard to monitor IoT sensors in real-time.', tech: ['React','WebSocket'], github:'#', demo:'#' },
  { id: 11, title: 'Food Delivery', desc: 'Food ordering app with delivery tracking.', tech: ['Flutter','Maps'], github:'#', demo:'#' },
  { id: 12, title: 'Mini Games', desc: 'Collection of small casual games.', tech: ['Flutter','Dart'], github:'#', demo:'#' }
]

export default function Portfolio(){
  return (
    <div className="min-h-screen bg-gradient-to-br from-gray-50 to-white text-gray-900">
      <header className="max-w-5xl mx-auto p-6 flex items-center justify-between">
        <div>
          <h1 className="text-2xl font-extrabold tracking-tight">M Zahoor</h1>
          <p className="text-sm text-gray-600">BSc Computer Science • Flutter Developer</p>
        </div>
        <nav className="flex gap-4 items-center">
          <a href="#projects" className="px-4 py-2 rounded-lg bg-black text-white text-sm">Projects</a>
          <a href="#contact" className="text-sm text-gray-600">Contact</a>
        </nav>
      </header>

      <main className="max-w-5xl mx-auto p-6">
        <section className="grid grid-cols-1 md:grid-cols-2 gap-8 items-center py-12">
          <motion.div initial={{ opacity:0, x:-20 }} animate={{ opacity:1, x:0 }} transition={{ delay:0.1 }}>
            <h2 className="text-4xl font-bold leading-tight">Hi — I’m M Zahoor.</h2>
            <p className="mt-4 text-gray-700">I build beautiful, high-performance mobile apps with Flutter and bring designs to life. I have a BSc in Computer Science and over 1 year of professional experience. I’ve worked on 12+ projects spanning e-commerce, chat, finance, and more.</p>

            <div className="mt-6 flex gap-3">
              <a href="mailto:mzahoor575@gmail.com" className="px-4 py-2 rounded-md border border-gray-900 text-sm">mzahoor575@gmail.com</a>
              <a href="tel:+923365884687" className="px-4 py-2 rounded-md bg-gray-900 text-white text-sm">+92 336 5884687</a>
            </div>

            <div className="mt-6 text-sm text-gray-600">
              <p><strong>Education:</strong> BSc Computer Science</p>
              <p><strong>Experience:</strong> 1+ year (Flutter)</p>
              <p className="mt-2">Looking for freelance or full-time opportunities — open to remote roles.</p>
            </div>
          </motion.div>

          <motion.div className="bg-white rounded-2xl shadow-lg p-6" initial={{ opacity:0, scale:0.98 }} animate={{ opacity:1, scale:1 }} transition={{ delay:0.2 }}>
            <h3 className="text-lg font-semibold">Top skills</h3>
            <div className="mt-4 grid grid-cols-2 gap-2 text-sm">
              <span className="p-2 rounded-md border">Flutter</span>
              <span className="p-2 rounded-md border">Dart</span>
              <span className="p-2 rounded-md border">REST APIs</span>
              <span className="p-2 rounded-md border">Firebase</span>
              <span className="p-2 rounded-md border">Git & GitHub</span>
              <span className="p-2 rounded-md border">UI/UX</span>
            </div>

            <div className="mt-6">
              <h4 className="text-sm font-medium">Quick stats</h4>
              <div className="mt-3 flex gap-4">
                <div className="text-center">
                  <div className="text-2xl font-bold">12+</div>
                  <div className="text-xs text-gray-500">Projects</div>
                </div>
                <div className="text-center">
                  <div className="text-2xl font-bold">1+</div>
                  <div className="text-xs text-gray-500">Years exp</div>
                </div>
              </div>
            </div>
          </motion.div>
        </section>

        <section id="projects" className="py-8">
          <h3 className="text-2xl font-semibold">Selected projects</h3>
          <p className="text-sm text-gray-600 mt-2">A snapshot of projects I built — click to view code or demo.</p>

          <div className="mt-6 grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
            {projects.map(p => (
              <motion.article key={p.id} whileHover={{ y:-6 }} className="bg-white rounded-2xl p-5 shadow transition-shadow">
                <h4 className="font-semibold">{p.title}</h4>
                <p className="text-sm text-gray-600 mt-2">{p.desc}</p>
                <div className="mt-3 flex flex-wrap gap-2 text-xs">
                  {p.tech.map(t => (
                    <span key={t} className="px-2 py-1 rounded-full border">{t}</span>
                  ))}
                </div>
                <div className="mt-4 flex gap-2">
                  <a href={p.github} className="text-sm underline">Code</a>
                  <a href={p.demo} className="text-sm underline">Live</a>
                </div>
              </motion.article>
            ))}
          </div>

          <div className="mt-6 text-center">
            <a href="#contact" className="px-5 py-2 rounded-full bg-black text-white">Hire me / Contact</a>
          </div>
        </section>

        <section id="contact" className="py-12">
          <h3 className="text-2xl font-semibold">Contact</h3>
          <div className="mt-4 grid grid-cols-1 md:grid-cols-2 gap-6">
            <div className="bg-white p-6 rounded-2xl shadow">
              <p className="text-sm text-gray-700">Email</p>
              <a href="mailto:mzahoor575@gmail.com" className="block mt-2 font-medium">mzahoor575@gmail.com</a>

              <p className="text-sm text-gray-700 mt-4">Phone</p>
              <a href="tel:+923365884687" className="block mt-2 font-medium">+92 336 5884687</a>

              <p className="text-sm text-gray-700 mt-4">Location</p>
              <div className="mt-2 text-sm font-medium">Karachi, Pakistan</div>
            </div>

            <motion.form className="bg-white p-6 rounded-2xl shadow space-y-3" onSubmit={(e)=>{e.preventDefault(); alert('Thanks! I will contact you soon.')}}>
              <label className="block text-sm">Your name</label>
              <input className="w-full p-2 border rounded-md" placeholder="Your name" required />

              <label className="block text-sm">Your email</label>
              <input type="email" className="w-full p-2 border rounded-md" placeholder="you@example.com" required />

              <label className="block text-sm">Message</label>
              <textarea className="w-full p-2 border rounded-md" rows={4} placeholder="Hi M Zahoor..." required />

              <div className="text-right">
                <button className="px-4 py-2 rounded-md bg-black text-white">Send message</button>
              </div>
            </motion.form>
          </div>
        </section>

        <footer className="py-8 text-center text-sm text-gray-500">© {new Date().getFullYear()} M Zahoor — Built with ❤️ and Flutter experience</footer>
      </main>
    </div>
  )
}
