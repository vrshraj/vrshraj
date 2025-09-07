import React from 'react';
import { motion } from 'framer-motion';

const aboutVariants = {
  hidden: { opacity: 0, y: 40 },
  visible: { opacity: 1, y: 0, transition: { duration: 0.8 } }
};

export default function AboutSection() {
  return (
    <motion.section
      className="about-section"
      initial="hidden"
      animate="visible"
      variants={aboutVariants}
    >
      <h2>About Me</h2>
      <p>
        <strong>Freelancer Web Developer</strong> & <strong>ML Student</strong>
      </p>
      <p>
        <strong>Skills:</strong> Python, AI Tools, Prompt Writing
      </p>
      <p>
        {/* TODO: Add more info about yourself here */}
        [You can fill in more details about your background, interests, and experience.]
      </p>
      {/* Example animation: Professional fade-in or some engaging effect */}
    </motion.section>
  );
}
