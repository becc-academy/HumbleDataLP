<script setup lang="ts">
import logo from '../assets/logo.png'
import coverImage from '../assets/cover.jpeg'

const handleRegister = () => {
  window.open('https://bit.ly/HDW1025', '_blank')
}

const features = [
  {
    title: 'Data Cleaning & Preparation',
    description: 'Master the art of transforming raw data into actionable insights using industry-standard techniques.'
  },
  {
    title: 'Advanced Analytics',
    description: 'Learn to identify patterns, trends, and anomalies that drive strategic decision-making.'
  },
  {
    title: 'Data Visualization',
    description: 'Create compelling visual narratives that communicate complex findings to any audience.'
  },
  {
    title: 'Python Fundamentals',
    description: 'Build a solid foundation in Python programming tailored specifically for data analysis.'
  }
]

const audience = [
  {
    title: 'Students & Recent Graduates',
    description: 'Gain practical skills that complement your academic knowledge and boost your career prospects.'
  },
  {
    title: 'Career Changers',
    description: 'Transition into data science with confidence through structured, beginner-friendly learning.'
  },
  {
    title: 'Business Professionals',
    description: 'Enhance your decision-making capabilities with data-driven insights and analysis.'
  },
  {
    title: 'Creative Professionals',
    description: 'Integrate data skills into your creative workflow for more impactful, informed work.'
  }
]

const schedule = [
  { time: '13:00', title: 'Welcome & Orientation', description: 'Introduction to the workshop structure and learning objectives' },
  { time: '13:30', title: 'Foundation Building', description: 'Core concepts and hands-on exercises with mentor guidance' },
  { time: '14:30', title: 'Interactive Session', description: 'Collaborative learning and peer discussion' },
  { time: '14:45', title: 'Advanced Techniques', description: 'Deep dive into practical applications and real-world scenarios' },
  { time: '15:45', title: 'Q&A & Next Steps', description: 'Address questions and outline your continued learning path' },
  { time: '16:00', title: 'Wrap-up', description: 'Summary and community invitation' }
]
</script>

<template>
  <div class="min-h-screen bg-humble-brown text-white">
    <!-- Animated Background Pattern -->
    <div class="fixed inset-0 bg-[radial-gradient(ellipse_80%_80%_at_50%_-20%,rgba(238,185,70,0.08),transparent)]"></div>
    <div class="fixed inset-0 overflow-hidden pointer-events-none">
      <div class="absolute top-20 right-20 w-96 h-96 bg-humble-yellow/10 rounded-full blur-3xl animate-pulse-glow"></div>
      <div class="absolute bottom-40 left-20 w-80 h-80 bg-humble-red/10 rounded-full blur-3xl animate-pulse-glow" style="animation-delay: 1s"></div>
    </div>
    
    <!-- Navigation -->
    <nav class="relative bg-white border-b-4 border-humble-yellow shadow-lg">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-6">
        <div class="flex items-center justify-between">
          <div class="flex items-center space-x-4 animate__animated animate__fadeInLeft">
            <img :src="logo" alt="Humble Data Workshop" class="h-16 w-auto" />
            <span class="text-2xl font-bold text-humble-brown">Humble Data Workshop</span>
          </div>
          <button @click="handleRegister" class="px-8 py-3.5 bg-humble-yellow text-humble-brown rounded-lg font-black text-lg hover:bg-humble-red hover:text-white transition-all duration-300 transform hover:scale-110 shadow-lg hover:shadow-humble-red/50 animate__animated animate__fadeInRight">
            Register Now
          </button>
        </div>
      </div>
    </nav>

    <!-- Hero Section -->
    <section class="relative">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 pt-20 pb-24">
        <div class="grid lg:grid-cols-2 gap-16 items-center">
          <!-- Left Content -->
          <div v-motion :initial="{ opacity: 0, y: 40 }" :enter="{ opacity: 1, y: 0, transition: { duration: 800, delay: 200 } }">
            <div class="inline-flex items-center space-x-2 bg-humble-yellow/20 border border-humble-yellow/40 rounded-full px-4 py-2 mb-8 animate__animated animate__bounceIn animate__delay-1s">
              <span class="w-2 h-2 bg-humble-yellow rounded-full animate-pulse"></span>
              <span class="text-sm text-humble-yellow font-semibold">Free Workshop • November 22, 2025</span>
            </div>
            
            <h1 class="text-5xl sm:text-6xl lg:text-7xl font-bold leading-tight mb-6 animate__animated animate__fadeInUp">
              Master Data Analysis
              <span class="block text-transparent bg-clip-text bg-gradient-to-r from-humble-yellow to-humble-red">
                in One Afternoon
              </span>
            </h1>
            
            <p class="text-xl text-humble-gray mb-8 leading-relaxed max-w-xl animate__animated animate__fadeInUp animate__delay-1s">
              Join Becc Academy's intensive workshop and learn to transform raw data into actionable insights. 
              No prior experience required.
            </p>

            <div class="flex flex-col sm:flex-row gap-4 mb-12 animate__animated animate__fadeInUp animate__delay-1s">
              <button @click="handleRegister" class="group relative px-8 py-4 bg-humble-yellow text-humble-brown rounded-lg font-bold overflow-hidden transition-all duration-300 hover:scale-110 hover:shadow-2xl hover:shadow-humble-yellow/50 hover:bg-humble-red hover:text-white">
                <span class="relative z-10">Register for Free</span>
              </button>
              <a href="#features" class="px-8 py-4 bg-white/5 border border-humble-yellow/30 rounded-lg font-semibold hover:bg-humble-yellow/10 hover:border-humble-yellow transition-all duration-300 text-center">
                Learn More
              </a>
            </div>

            <!-- Quick Info -->
            <div class="grid grid-cols-3 gap-6 pt-8 border-t border-humble-yellow/20 animate__animated animate__fadeIn animate__delay-2s">
              <div class="transform hover:scale-110 transition-transform duration-300">
                <div class="text-2xl font-bold text-humble-yellow mb-1">3 Hours</div>
                <div class="text-sm text-humble-gray">Duration</div>
              </div>
              <div class="transform hover:scale-110 transition-transform duration-300">
                <div class="text-2xl font-bold text-humble-yellow mb-1">Virtual</div>
                <div class="text-sm text-humble-gray">Location</div>
              </div>
              <div class="transform hover:scale-110 transition-transform duration-300">
                <div class="text-2xl font-bold text-humble-yellow mb-1">13:00 GMT</div>
                <div class="text-sm text-humble-gray">Start Time</div>
              </div>
            </div>
          </div>

          <!-- Right Content - Hero Image -->
          <div v-motion :initial="{ opacity: 0, x: 40 }" :enter="{ opacity: 1, x: 0, transition: { duration: 800, delay: 400 } }" class="relative animate-float">
            <div class="relative rounded-2xl overflow-hidden border-4 border-humble-yellow/30 shadow-2xl shadow-humble-yellow/20">
              <img :src="coverImage" alt="Data Workshop" class="w-full h-auto" />
              <div class="absolute inset-0 bg-gradient-to-t from-humble-brown via-humble-brown/40 to-transparent"></div>
              
              <!-- Floating Stats -->
              <div class="absolute bottom-6 left-6 right-6 animate__animated animate__fadeInUp animate__delay-2s">
                <div class="bg-humble-brown/90 backdrop-blur-md border-2 border-humble-yellow/40 rounded-xl p-6">
                  <div class="grid grid-cols-2 gap-6">
                    <div class="transform hover:scale-110 transition-transform duration-300">
                      <div class="text-3xl font-bold text-humble-yellow mb-1">500+</div>
                      <div class="text-sm text-humble-gray">Active Learners</div>
                    </div>
                    <div class="transform hover:scale-110 transition-transform duration-300">
                      <div class="text-3xl font-bold text-humble-yellow mb-1">100%</div>
                      <div class="text-sm text-humble-gray">Free Access</div>
                    </div>
                  </div>
                </div>
              </div>
            </div>

            <!-- Decorative Elements -->
            <div class="absolute -top-4 -right-4 w-32 h-32 bg-humble-yellow rounded-full opacity-30 blur-3xl animate-pulse-glow"></div>
            <div class="absolute -bottom-4 -left-4 w-40 h-40 bg-humble-red rounded-full opacity-30 blur-3xl animate-pulse-glow" style="animation-delay: 1s"></div>
          </div>
        </div>
      </div>
    </section>

    <!-- Trusted By Section -->
    <section class="relative py-16 bg-white border-y-4 border-humble-yellow shadow-inner">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <p class="text-center text-sm text-humble-brown/60 mb-8 tracking-wider font-bold">ORGANIZED BY</p>
        <div class="flex justify-center">
          <div class="text-4xl font-black text-humble-red animate__animated animate__fadeIn animate__delay-1s">Becc Academy</div>
        </div>
      </div>
    </section>

    <!-- Features Section -->
    <section id="features" class="relative py-24">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center mb-16">
          <h2 class="text-4xl sm:text-5xl font-bold mb-4 text-humble-yellow animate__animated animate__fadeInDown">
            What You'll Learn
          </h2>
          <p class="text-xl text-humble-gray max-w-2xl mx-auto animate__animated animate__fadeIn animate__delay-1s">
            Comprehensive curriculum designed to take you from beginner to confident data analyst
          </p>
        </div>

        <div class="grid md:grid-cols-2 gap-8">
          <div 
            v-for="(feature, index) in features" 
            :key="index"
            v-motion 
            :initial="{ opacity: 0, y: 40 }" 
            :visible-once="{ opacity: 1, y: 0, transition: { duration: 600, delay: index * 150 } }"
            class="group relative bg-white/5 border-2 border-humble-yellow/20 rounded-2xl p-8 hover:bg-humble-yellow/10 hover:border-humble-yellow hover:scale-105 transition-all duration-500 shadow-lg hover:shadow-humble-yellow/30"
          >
            <div class="absolute inset-0 bg-gradient-to-br from-humble-red/10 to-transparent rounded-2xl opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
            <div class="relative">
              <h3 class="text-2xl font-bold mb-3 text-white group-hover:text-humble-yellow transition-colors duration-300">{{ feature.title }}</h3>
              <p class="text-humble-gray leading-relaxed">{{ feature.description }}</p>
            </div>
          </div>
        </div>

        <!-- Tools Section -->
        <div class="mt-16 bg-gradient-to-br from-humble-red/20 to-humble-yellow/20 border-2 border-humble-yellow/40 rounded-2xl p-12 animate__animated animate__fadeInUp">
          <h3 class="text-3xl font-bold mb-8 text-center text-humble-yellow">Your Professional Toolkit</h3>
          <div class="grid md:grid-cols-3 gap-8">
            <div class="text-center transform hover:scale-110 transition-all duration-500">
              <div class="text-5xl font-bold text-humble-yellow mb-2 animate__animated animate__zoomIn animate__delay-1s">Python</div>
              <p class="text-humble-gray">Industry-standard programming language</p>
            </div>
            <div class="text-center transform hover:scale-110 transition-all duration-500">
              <div class="text-5xl font-bold text-humble-yellow mb-2 animate__animated animate__zoomIn animate__delay-2s">Jupyter</div>
              <p class="text-humble-gray">Interactive development environment</p>
            </div>
            <div class="text-center transform hover:scale-110 transition-all duration-500">
              <div class="text-5xl font-bold text-humble-yellow mb-2 animate__animated animate__zoomIn animate__delay-3s">Pandas</div>
              <p class="text-humble-gray">Data manipulation framework</p>
            </div>
          </div>
          <div class="mt-8 text-center">
            <p class="text-white text-lg font-semibold">
              Small group sessions with dedicated mentors ensuring personalized attention and support
            </p>
          </div>
        </div>
      </div>
    </section>

    <!-- Who Is This For Section -->
    <section class="relative py-24 bg-white">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center mb-16">
          <h2 class="text-4xl sm:text-5xl font-bold mb-4 text-humble-brown animate__animated animate__fadeInDown">
            Who Should Attend
          </h2>
          <p class="text-xl text-humble-brown/70 max-w-2xl mx-auto animate__animated animate__fadeIn animate__delay-1s">
            This workshop is designed for anyone ready to add data skills to their professional toolkit
          </p>
        </div>

        <div class="grid md:grid-cols-2 gap-6">
          <div 
            v-for="(item, index) in audience" 
            :key="index"
            v-motion 
            :initial="{ opacity: 0, scale: 0.9 }" 
            :visible-once="{ opacity: 1, scale: 1, transition: { duration: 600, delay: index * 150 } }"
            class="bg-gradient-to-br from-humble-yellow/10 to-humble-red/10 border-2 border-humble-yellow/50 rounded-xl p-8 hover:border-humble-red hover:bg-humble-yellow/20 hover:scale-105 transition-all duration-500 shadow-lg hover:shadow-humble-yellow/50"
          >
            <h3 class="text-2xl font-bold mb-3 text-humble-red">{{ item.title }}</h3>
            <p class="text-humble-brown leading-relaxed">{{ item.description }}</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Schedule Section -->
    <section class="relative py-24">
      <div class="max-w-5xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center mb-16">
          <h2 class="text-4xl sm:text-5xl font-bold mb-4 text-humble-yellow animate__animated animate__fadeInDown">
            Workshop Schedule
          </h2>
          <p class="text-xl text-humble-gray animate__animated animate__fadeIn animate__delay-1s">
            Three intensive hours of hands-on learning
          </p>
        </div>

        <div class="space-y-4">
          <div 
            v-for="(item, index) in schedule" 
            :key="index"
            v-motion 
            :initial="{ opacity: 0, x: -40 }" 
            :visible-once="{ opacity: 1, x: 0, transition: { duration: 600, delay: index * 100 } }"
            class="flex gap-6 items-start bg-white/5 border-2 border-humble-yellow/20 rounded-xl p-6 hover:bg-humble-yellow/10 hover:border-humble-yellow hover:scale-105 hover:shadow-lg hover:shadow-humble-yellow/30 transition-all duration-500"
          >
            <div class="flex-shrink-0 w-24 text-center">
              <div class="text-2xl font-black text-humble-yellow bg-humble-red/30 rounded-lg py-2 px-3 border border-humble-yellow/50">{{ item.time }}</div>
            </div>
            <div class="flex-grow border-l-4 border-humble-red/50 pl-6">
              <h3 class="text-xl font-bold mb-2 text-white">{{ item.title }}</h3>
              <p class="text-humble-gray">{{ item.description }}</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- FAQ Section -->
    <section class="relative py-24 bg-white border-y-4 border-humble-yellow">
      <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center mb-16">
          <h2 class="text-4xl sm:text-5xl font-bold mb-4 text-humble-brown animate__animated animate__fadeInDown">
            Frequently Asked Questions
          </h2>
        </div>

        <div class="space-y-6">
          <div v-motion :initial="{ opacity: 0, y: 30 }" :visible-once="{ opacity: 1, y: 0, transition: { duration: 600 } }" class="bg-gradient-to-br from-humble-yellow/10 to-humble-red/10 border-2 border-humble-yellow/50 rounded-xl p-8 hover:border-humble-red hover:bg-humble-yellow/20 hover:scale-105 transition-all duration-500 shadow-lg">
            <h3 class="text-2xl font-bold mb-4 text-humble-red">What do I need to participate?</h3>
            <p class="text-humble-brown leading-relaxed">
              A computer with internet access. All software and tools will be provided through cloud-based platforms.
            </p>
          </div>

          <div v-motion :initial="{ opacity: 0, y: 30 }" :visible-once="{ opacity: 1, y: 0, transition: { duration: 600, delay: 150 } }" class="bg-gradient-to-br from-humble-yellow/10 to-humble-red/10 border-2 border-humble-yellow/50 rounded-xl p-8 hover:border-humble-red hover:bg-humble-yellow/20 hover:scale-105 transition-all duration-500 shadow-lg">
            <h3 class="text-2xl font-bold mb-4 text-humble-red">Is this really free?</h3>
            <p class="text-humble-brown leading-relaxed">
              Yes, completely free. We believe in making data education accessible to everyone. Our mentors volunteer their time to support the community.
            </p>
          </div>

          <div v-motion :initial="{ opacity: 0, y: 30 }" :visible-once="{ opacity: 1, y: 0, transition: { duration: 600, delay: 300 } }" class="bg-gradient-to-br from-humble-yellow/10 to-humble-red/10 border-2 border-humble-yellow/50 rounded-xl p-8 hover:border-humble-red hover:bg-humble-yellow/20 hover:scale-105 transition-all duration-500 shadow-lg">
            <h3 class="text-2xl font-bold mb-4 text-humble-red">Do I need programming experience?</h3>
            <p class="text-humble-brown leading-relaxed">
              No prior experience required. The workshop is designed for complete beginners, with materials that allow you to progress at your own pace.
            </p>
          </div>
        </div>
      </div>
    </section>

    <!-- CTA Section -->
    <section class="relative py-32">
      <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
        <div v-motion :initial="{ opacity: 0, scale: 0.9 }" :visible-once="{ opacity: 1, scale: 1, transition: { duration: 800 } }" class="bg-gradient-to-br from-humble-red/30 to-humble-yellow/30 border-4 border-humble-yellow/50 rounded-3xl p-16 shadow-2xl shadow-humble-yellow/20">
          <h2 class="text-5xl sm:text-6xl font-black mb-6 text-humble-yellow animate__animated animate__pulse animate__infinite animate__slow">
            Ready to Start?
          </h2>
          <p class="text-xl text-white mb-12 max-w-2xl mx-auto leading-relaxed">
            Join hundreds of learners taking their first step into data analysis. 
            No experience needed, just curiosity and a laptop.
          </p>
          
          <button @click="handleRegister" class="px-16 py-6 bg-humble-yellow text-humble-brown rounded-xl text-2xl font-black hover:scale-110 transition-all duration-500 shadow-2xl hover:shadow-humble-yellow/50 hover:bg-humble-red hover:text-white animate__animated animate__bounceIn animate__delay-1s">
            Register for Free Workshop
          </button>

          <p class="mt-8 text-sm text-humble-gray font-semibold">
            Saturday, November 22, 2025 • 13:00-16:00 GMT • Virtual Event
          </p>
        </div>
      </div>
    </section>

    <!-- Footer -->
    <footer class="relative border-t-4 border-humble-yellow py-16 bg-white shadow-2xl">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="grid md:grid-cols-3 gap-12 mb-8">
          <!-- Brand Section -->
          <div class="flex flex-col items-center md:items-start gap-4 animate__animated animate__fadeInLeft">
            <div class="flex items-center space-x-4">
              <img :src="logo" alt="Humble Data Workshop" class="h-16 w-auto" />
              <div>
                <div class="font-black text-2xl text-humble-brown">Humble Data Workshop</div>
                <div class="text-sm text-humble-red font-semibold">Powered by Data Excellence</div>
              </div>
            </div>
            <p class="text-humble-brown/70 text-sm text-center md:text-left max-w-xs">
              Empowering everyone with data skills through free, accessible workshops and community support.
            </p>
          </div>

          <!-- Contact Section -->
          <div class="text-center animate__animated animate__fadeInUp">
            <h3 class="font-black text-lg text-humble-brown mb-4">Get In Touch</h3>
            <div class="space-y-3">
              <a href="tel:+233201233215" class="flex items-center justify-center gap-2 text-humble-brown hover:text-humble-red transition-colors duration-300">
                <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20">
                  <path d="M2 3a1 1 0 011-1h2.153a1 1 0 01.986.836l.74 4.435a1 1 0 01-.54 1.06l-1.548.773a11.037 11.037 0 006.105 6.105l.774-1.548a1 1 0 011.059-.54l4.435.74a1 1 0 01.836.986V17a1 1 0 01-1 1h-2C7.82 18 2 12.18 2 5V3z"/>
                </svg>
                <span class="font-semibold">+(233)-20-123-3215</span>
              </a>
              <p class="text-humble-brown text-base font-semibold">Organized by <span class="text-humble-red font-black">Becc Academy</span></p>
            </div>
          </div>

          <!-- Social Media Section -->
          <div class="text-center md:text-right animate__animated animate__fadeInRight">
            <h3 class="font-black text-lg text-humble-brown mb-4">Follow Us</h3>
            <div class="flex gap-4 justify-center md:justify-end mb-4">
              <a href="https://twitter.com/beccacademy" target="_blank" rel="noopener noreferrer" class="w-10 h-10 bg-humble-yellow rounded-full flex items-center justify-center hover:bg-humble-red hover:scale-110 transition-all duration-300 group">
                <svg class="w-5 h-5 text-humble-brown group-hover:text-white" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M18.244 2.25h3.308l-7.227 8.26 8.502 11.24H16.17l-5.214-6.817L4.99 21.75H1.68l7.73-8.835L1.254 2.25H8.08l4.713 6.231zm-1.161 17.52h1.833L7.084 4.126H5.117z"/>
                </svg>
              </a>
              <a href="https://www.instagram.com/beccacademy" target="_blank" rel="noopener noreferrer" class="w-10 h-10 bg-humble-yellow rounded-full flex items-center justify-center hover:bg-humble-red hover:scale-110 transition-all duration-300 group">
                <svg class="w-5 h-5 text-humble-brown group-hover:text-white" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z"/>
                </svg>
              </a>
              <a href="https://www.facebook.com/beccacademy" target="_blank" rel="noopener noreferrer" class="w-10 h-10 bg-humble-yellow rounded-full flex items-center justify-center hover:bg-humble-red hover:scale-110 transition-all duration-300 group">
                <svg class="w-5 h-5 text-humble-brown group-hover:text-white" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M24 12.073c0-6.627-5.373-12-12-12s-12 5.373-12 12c0 5.99 4.388 10.954 10.125 11.854v-8.385H7.078v-3.47h3.047V9.43c0-3.007 1.792-4.669 4.533-4.669 1.312 0 2.686.235 2.686.235v2.953H15.83c-1.491 0-1.956.925-1.956 1.874v2.25h3.328l-.532 3.47h-2.796v8.385C19.612 23.027 24 18.062 24 12.073z"/>
                </svg>
              </a>
              <a href="https://www.linkedin.com/company/beccacademy/" target="_blank" rel="noopener noreferrer" class="w-10 h-10 bg-humble-yellow rounded-full flex items-center justify-center hover:bg-humble-red hover:scale-110 transition-all duration-300 group">
                <svg class="w-5 h-5 text-humble-brown group-hover:text-white" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065 0-1.138.92-2.063 2.063-2.063 1.14 0 2.064.925 2.064 2.063 0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/>
                </svg>
              </a>
            </div>
            <p class="text-humble-brown/70 text-xs">@beccacademy</p>
          </div>
        </div>

        <!-- Bottom Bar -->
        <div class="border-t border-humble-yellow/30 pt-6 text-center">
          <p class="text-humble-brown/70 text-sm">© 2025 Becc Academy. All rights reserved.</p>
        </div>
      </div>
    </footer>
  </div>
</template>
