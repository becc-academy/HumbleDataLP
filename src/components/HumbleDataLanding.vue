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
        <div class="flex flex-col md:flex-row justify-between items-center gap-8">
          <div class="flex flex-col items-center md:items-start gap-4 animate__animated animate__fadeInLeft">
            <div class="flex items-center space-x-4">
              <img :src="logo" alt="Humble Data Workshop" class="h-16 w-auto" />
              <div>
                <div class="font-black text-2xl text-humble-brown">Humble Data Workshop</div>
                <div class="text-sm text-humble-red font-semibold">Powered by Data Excellence</div>
              </div>
            </div>
          </div>
          
          <div class="text-center md:text-right animate__animated animate__fadeInRight">
            <p class="text-humble-brown text-base mb-2 font-semibold">Organized by <span class="text-humble-red font-black">Becc Academy</span></p>
            <p class="text-humble-brown/70 text-sm">© 2025 All rights reserved</p>
            <div class="mt-4 flex gap-4 justify-center md:justify-end">
              <button class="px-6 py-2 bg-humble-yellow text-humble-brown rounded-lg font-bold hover:bg-humble-red hover:text-white transition-all duration-300 transform hover:scale-110">
                Contact Us
              </button>
            </div>
          </div>
        </div>
      </div>
    </footer>
  </div>
</template>
