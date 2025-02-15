import React from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { motion } from "framer-motion";
import { FaGithub, FaLinkedin, FaEnvelope, FaCode, FaProjectDiagram } from "react-icons/fa";

const Portfolio = () => {
  return (
    <div className="min-h-screen bg-gray-900 text-white p-6 flex flex-col items-center">
      <motion.h1
        className="text-5xl font-extrabold mb-6 text-center"
        initial={{ opacity: 0, y: -50 }}
        animate={{ opacity: 1, y: 0 }}
        transition={{ duration: 1 }}
      >
        Welcome to My Portfolio
      </motion.h1>
      
      <motion.p
        className="text-xl text-gray-300 text-center max-w-3xl mb-6"
        initial={{ opacity: 0 }}
        animate={{ opacity: 1 }}
        transition={{ duration: 1.5 }}
      >
        Hi! I'm a passionate Frontend Developer with a strong background in creating dynamic and responsive web applications.
        I thrive in building elegant and efficient user experiences, leveraging modern frameworks and best practices.
        My journey into web development started with a love for design and problem-solving, and today, I bring that passion
        into every project I work on.
      </motion.p>
      
      <Card className="bg-gray-800 max-w-2xl p-8 rounded-2xl shadow-xl">
        <CardContent>
          <motion.p
            className="text-lg mb-6 text-gray-300"
            initial={{ opacity: 0 }}
            animate={{ opacity: 1 }}
            transition={{ duration: 1.5 }}
          >
            I specialize in crafting interactive, user-friendly web applications using cutting-edge technologies like React, Tailwind CSS, and TypeScript.
          </motion.p>
          
          <h2 className="text-3xl font-semibold mb-4 flex items-center">
            <FaCode className="mr-2" /> Skills
          </h2>
          <ul className="grid grid-cols-2 gap-4 text-lg mb-6">
            <li>React.js & Next.js</li>
            <li>JavaScript & TypeScript</li>
            <li>Redux & Context API</li>
            <li>GraphQL & REST APIs</li>
            <li>Tailwind CSS & Styled Components</li>
            <li>Accessibility & Performance Optimization</li>
          </ul>
          
          <h2 className="text-3xl font-semibold mb-4 flex items-center">
            <FaProjectDiagram className="mr-2" /> Projects
          </h2>
          <ul className="space-y-4 mb-6">
            <li className="bg-gray-700 p-4 rounded-lg shadow-md"> <strong>Portfolio Website</strong> - A responsive personal website showcasing my skills and work.</li>
            <li className="bg-gray-700 p-4 rounded-lg shadow-md"> <strong>E-commerce Store</strong> - A full-stack e-commerce application with payment integration.</li>
            <li className="bg-gray-700 p-4 rounded-lg shadow-md"> <strong>Blog CMS</strong> - A content management system for writing and managing blogs.</li>
          </ul>
          
          <h2 className="text-3xl font-semibold mb-4 flex items-center">
            Contact Me
          </h2>
          <div className="flex space-x-6 text-3xl">
            <a href="#" className="text-white hover:text-gray-400"><FaGithub /></a>
            <a href="#" className="text-blue-500 hover:text-blue-300"><FaLinkedin /></a>
            <a href="mailto:your.email@example.com" className="text-red-500 hover:text-red-300"><FaEnvelope /></a>
          </div>
        </CardContent>
      </Card>
    </div>
  );
};

export default Portfolio;
