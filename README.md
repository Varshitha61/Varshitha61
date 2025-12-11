import React, { useState, useEffect } from 'react';
import { Play, Code, Lightbulb, Zap, Coffee, Flame, Star, Award, TrendingUp, Target, Heart, Sparkles } from 'lucide-react';

export default function GitHubProfile() {
  const [time, setTime] = useState(new Date());
  const [activeProject, setActiveProject] = useState(0);

  useEffect(() => {
    const timer = setInterval(() => setTime(new Date()), 1000);
    return () => clearInterval(timer);
  }, []);

  const timeline = [
    { year: '2023', event: 'Started B.E. CSE Journey', color: 'bg-blue-500' },
    { year: '2024', event: 'Full-Stack Intern @ Learnlogicify', color: 'bg-green-500' },
    { year: '2024', event: 'LeetCode Rating 2055 (Top 14.5%)', color: 'bg-orange-500' },
    { year: '2025', event: 'Research Paper @ ICEE 2025', color: 'bg-purple-500' },
    { year: '2025', event: 'Building the Future...', color: 'bg-pink-500' }
  ];

  const expertise = [
    { domain: 'Full-Stack Development', skills: ['React', 'Node.js', 'Express', 'MySQL'], icon: '🌐', color: 'border-blue-500' },
    { domain: 'Artificial Intelligence', skills: ['Gemini API', 'Scikit-learn', 'ML Models'], icon: '🤖', color: 'border-purple-500' },
    { domain: 'IoT & Embedded', skills: ['Microcontrollers', 'Sensors', 'Embedded C'], icon: '📡', color: 'border-green-500' },
    { domain: 'Problem Solving', skills: ['Data Structures', 'Algorithms', 'Competitive Coding'], icon: '🧩', color: 'border-orange-500' }
  ];

  const achievements = [
    { title: 'LeetCode Knight', desc: 'Max Rating 2055', icon: '🏰', stat: 'Top 14.5%' },
    { title: 'Code Warrior', desc: '460+ Problems', icon: '⚔️', stat: '3 Platforms' },
    { title: 'Published Researcher', desc: 'ICEE 2025', icon: '📜', stat: 'IoT Domain' },
    { title: 'Tech Builder', desc: '10+ Projects', icon: '🔨', stat: 'Full-Stack' }
  ];

  const showcase = [
    {
      name: 'Pill Sense',
      tagline: 'Healthcare meets IoT',
      icon: '💊',
      description: 'Smart medication tracking system with real-time monitoring',
      impact: 'Research Paper Published',
      tech: ['IoT', 'Embedded C', 'Sensors'],
      color: 'from-violet-600 to-purple-600'
    },
    {
      name: 'SpendWiser',
      tagline: 'AI-powered finances',
      icon: '💰',
      description: 'Intelligent receipt scanning and spending analytics',
      impact: 'Gemini AI Integration',
      tech: ['React', 'TypeScript', 'AI'],
      color: 'from-cyan-600 to-blue-600'
    },
    {
      name: 'Cafe Aroma',
      tagline: 'Full-stack delight',
      icon: '☕',
      description: 'Complete café system with AI virtual assistant',
      impact: 'Serverless Architecture',
      tech: ['React', 'Vite', 'AI'],
      color: 'from-amber-600 to-orange-600'
    }
  ];

  return (
    <div className="min-h-screen bg-white text-gray-900">
      {/* Hero Section with Geometric Design */}
      <div className="relative overflow-hidden bg-gradient-to-br from-indigo-50 via-purple-50 to-pink-50">
        <div className="absolute inset-0">
          <div className="absolute top-20 left-20 w-72 h-72 bg-purple-200 rounded-full mix-blend-multiply filter blur-xl opacity-70 animate-blob"></div>
          <div className="absolute top-40 right-20 w-72 h-72 bg-yellow-200 rounded-full mix-blend-multiply filter blur-xl opacity-70 animate-blob animation-delay-2000"></div>
          <div className="absolute bottom-20 left-40 w-72 h-72 bg-pink-200 rounded-full mix-blend-multiply filter blur-xl opacity-70 animate-blob animation-delay-4000"></div>
        </div>

        <div className="relative max-w-7xl mx-auto px-8 py-20">
          <div className="text-center mb-12">
            <div className="inline-block mb-6">
              <div className="w-32 h-32 bg-gradient-to-br from-indigo-600 to-purple-600 rounded-3xl flex items-center justify-center text-white text-5xl font-bold shadow-2xl transform rotate-3 hover:rotate-6 transition-transform">
                SV
              </div>
            </div>
            <h1 className="text-6xl font-extrabold mb-4">
              <span className="bg-gradient-to-r from-indigo-600 via-purple-600 to-pink-600 bg-clip-text text-transparent">
                S Varshitha
              </span>
            </h1>
            <p className="text-2xl text-gray-600 mb-6">Software Engineer • Problem Solver • Tech Enthusiast</p>
            <div className="flex gap-4 justify-center flex-wrap">
              <span className="px-6 py-2 bg-white rounded-full shadow-md text-sm font-semibold text-gray-700 border-2 border-indigo-100">
                🎓 B.E. CSE @ KIT Coimbatore
              </span>
              <span className="px-6 py-2 bg-white rounded-full shadow-md text-sm font-semibold text-gray-700 border-2 border-purple-100">
                📍 Coimbatore, India
              </span>
              <span className="px-6 py-2 bg-white rounded-full shadow-md text-sm font-semibold text-gray-700 border-2 border-pink-100">
                ⭐ CGPA 7.9
              </span>
            </div>
          </div>

          {/* Quick Stats Cards */}
          <div className="grid grid-cols-2 md:grid-cols-4 gap-6 max-w-5xl mx-auto">
            {[
              { icon: '🏆', value: '2055', label: 'LeetCode Max', color: 'bg-orange-100 border-orange-300' },
              { icon: '🎯', value: '460+', label: 'Problems', color: 'bg-blue-100 border-blue-300' },
              { icon: '📝', value: '1', label: 'Research', color: 'bg-purple-100 border-purple-300' },
              { icon: '🚀', value: '10+', label: 'Projects', color: 'bg-green-100 border-green-300' }
            ].map((stat, idx) => (
              <div key={idx} className={`${stat.color} border-2 rounded-2xl p-6 text-center transform hover:scale-105 transition-all shadow-md`}>
                <div className="text-4xl mb-2">{stat.icon}</div>
                <div className="text-3xl font-bold text-gray-800 mb-1">{stat.value}</div>
                <div className="text-sm text-gray-600">{stat.label}</div>
              </div>
            ))}
          </div>
        </div>
      </div>

      <div className="max-w-7xl mx-auto px-8 py-16">
        {/* About Section with Timeline */}
        <section className="mb-20">
          <h2 className="text-4xl font-bold mb-8 text-center bg-gradient-to-r from-indigo-600 to-purple-600 bg-clip-text text-transparent">
            My Journey
          </h2>
          <div className="relative">
            <div className="absolute left-1/2 transform -translate-x-1/2 h-full w-1 bg-gradient-to-b from-indigo-200 via-purple-200 to-pink-200"></div>
            <div className="space-y-8">
              {timeline.map((item, idx) => (
                <div key={idx} className={`flex items-center ${idx % 2 === 0 ? 'flex-row' : 'flex-row-reverse'} gap-8`}>
                  <div className={`flex-1 ${idx % 2 === 0 ? 'text-right' : 'text-left'}`}>
                    <div className="bg-white rounded-xl p-6 shadow-lg border-2 border-gray-100 inline-block">
                      <div className="text-sm text-gray-500 mb-2">{item.year}</div>
                      <div className="font-semibold text-gray-800">{item.event}</div>
                    </div>
                  </div>
                  <div className={`${item.color} w-6 h-6 rounded-full border-4 border-white shadow-lg z-10`}></div>
                  <div className="flex-1"></div>
                </div>
              ))}
            </div>
          </div>
        </section>

        {/* Expertise Cards */}
        <section className="mb-20">
          <h2 className="text-4xl font-bold mb-12 text-center bg-gradient-to-r from-purple-600 to-pink-600 bg-clip-text text-transparent">
            Areas of Expertise
          </h2>
          <div className="grid grid-cols-1 md:grid-cols-2 gap-8">
            {expertise.map((area, idx) => (
              <div key={idx} className={`bg-white rounded-2xl p-8 shadow-lg border-l-4 ${area.color} hover:shadow-2xl transition-all`}>
                <div className="flex items-center gap-4 mb-6">
                  <div className="text-5xl">{area.icon}</div>
                  <h3 className="text-2xl font-bold text-gray-800">{area.domain}</h3>
                </div>
                <div className="flex flex-wrap gap-2">
                  {area.skills.map((skill, i) => (
                    <span key={i} className="px-4 py-2 bg-gray-50 rounded-lg text-sm font-medium text-gray-700 border border-gray-200">
                      {skill}
                    </span>
                  ))}
                </div>
              </div>
            ))}
          </div>
        </section>

        {/* Achievement Badges */}
        <section className="mb-20">
          <h2 className="text-4xl font-bold mb-12 text-center bg-gradient-to-r from-orange-600 to-red-600 bg-clip-text text-transparent">
            Achievements Unlocked
          </h2>
          <div className="grid grid-cols-1 md:grid-cols-4 gap-6">
            {achievements.map((achievement, idx) => (
              <div key={idx} className="bg-gradient-to-br from-white to-gray-50 rounded-2xl p-6 shadow-lg border-2 border-gray-100 text-center hover:scale-105 transition-transform">
                <div className="text-6xl mb-4">{achievement.icon}</div>
                <h3 className="font-bold text-lg text-gray-800 mb-2">{achievement.title}</h3>
                <p className="text-sm text-gray-600 mb-2">{achievement.desc}</p>
                <span className="inline-block px-4 py-1 bg-indigo-100 text-indigo-700 rounded-full text-xs font-semibold">
                  {achievement.stat}
                </span>
              </div>
            ))}
          </div>
        </section>

        {/* Project Showcase */}
        <section className="mb-20">
          <h2 className="text-4xl font-bold mb-12 text-center bg-gradient-to-r from-green-600 to-teal-600 bg-clip-text text-transparent">
            Featured Work
          </h2>
          <div className="space-y-8">
            {showcase.map((project, idx) => (
              <div key={idx} className="bg-white rounded-3xl shadow-xl overflow-hidden border-2 border-gray-100 hover:shadow-2xl transition-all">
                <div className={`h-3 bg-gradient-to-r ${project.color}`}></div>
                <div className="p-8">
                  <div className="flex items-start gap-6">
                    <div className="text-7xl">{project.icon}</div>
                    <div className="flex-1">
                      <h3 className="text-3xl font-bold text-gray-800 mb-2">{project.name}</h3>
                      <p className={`text-lg font-semibold bg-gradient-to-r ${project.color} bg-clip-text text-transparent mb-4`}>
                        {project.tagline}
                      </p>
                      <p className="text-gray-600 mb-4">{project.description}</p>
                      <div className="flex items-center gap-3 mb-4">
                        <Award className="w-5 h-5 text-amber-500" />
                        <span className="font-semibold text-gray-700">{project.impact}</span>
                      </div>
                      <div className="flex flex-wrap gap-2">
                        {project.tech.map((tech, i) => (
                          <span key={i} className="px-4 py-2 bg-gray-100 rounded-full text-sm font-medium text-gray-700">
                            {tech}
                          </span>
                        ))}
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            ))}
          </div>
        </section>

        {/* Competitive Programming */}
        <section className="mb-20">
          <h2 className="text-4xl font-bold mb-12 text-center bg-gradient-to-r from-yellow-600 to-orange-600 bg-clip-text text-transparent">
            Competitive Coding
          </h2>
          <div className="grid grid-cols-1 md:grid-cols-3 gap-8">
            {[
              { platform: 'LeetCode', rating: '2055', badge: 'Top 14.5%', solved: '80+', color: 'from-orange-400 to-red-500', icon: '🟠' },
              { platform: 'CodeChef', rating: '1314', badge: '1 Star', solved: '380', color: 'from-amber-400 to-yellow-500', icon: '⭐' },
              { platform: 'Codeforces', rating: '965', badge: 'Pupil', solved: 'Active', color: 'from-blue-400 to-cyan-500', icon: '🔵' }
            ].map((cp, idx) => (
              <div key={idx} className="bg-white rounded-2xl p-8 shadow-lg border-2 border-gray-100">
                <div className="text-center">
                  <div className="text-5xl mb-4">{cp.icon}</div>
                  <h3 className="text-2xl font-bold text-gray-800 mb-4">{cp.platform}</h3>
                  <div className={`text-5xl font-extrabold bg-gradient-to-r ${cp.color} bg-clip-text text-transparent mb-2`}>
                    {cp.rating}
                  </div>
                  <div className="space-y-2">
                    <div className="px-4 py-2 bg-gray-50 rounded-lg">
                      <span className="font-semibold text-gray-700">{cp.badge}</span>
                    </div>
                    <div className="text-sm text-gray-600">{cp.solved} Problems</div>
                  </div>
                </div>
              </div>
            ))}
          </div>
        </section>

        {/* Contact CTA */}
        <section>
          <div className="bg-gradient-to-r from-indigo-600 via-purple-600 to-pink-600 rounded-3xl p-12 text-white text-center shadow-2xl">
            <h2 className="text-4xl font-bold mb-4">Let's Build Something Amazing!</h2>
            <p className="text-xl mb-8 text-indigo-100">
              Open to collaborations, opportunities, and innovative projects
            </p>
            <div className="flex gap-4 justify-center flex-wrap">
              <a href="mailto:varshithasomashekar22@gmail.com" className="px-8 py-4 bg-white text-purple-600 rounded-xl font-bold shadow-lg hover:scale-105 transition-transform">
                📧 Email Me
              </a>
              <a href="https://linkedin.com/in/S-Varshitha" className="px-8 py-4 bg-white/10 backdrop-blur-sm rounded-xl font-bold border-2 border-white hover:scale-105 transition-transform">
                💼 LinkedIn
              </a>
              <a href="https://github.com/Varshitha61" className="px-8 py-4 bg-white/10 backdrop-blur-sm rounded-xl font-bold border-2 border-white hover:scale-105 transition-transform">
                🐙 GitHub
              </a>
            </div>
            <div className="mt-8 text-indigo-100">
              📱 +91 7892598335
            </div>
          </div>
        </section>
      </div>
    </div>
  );
}
