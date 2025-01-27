import React from "react";
import { motion } from "framer-motion";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";

export default function ApologyWebsite() {
  const navigateToLetter = () => {
    window.open("https://docs.google.com/document/d/1C4Rr4XVLv8BG1DyEbyg5Krg_r7b50832LhRsDak1brU/edit?usp=sharing", "_blank");
  };

  const navigateToSong = () => {
    window.open("https://www.youtube.com/watch?v=VuNIsY6JdUw", "_blank");
  };

  return (
    <div className="min-h-screen flex flex-col items-center justify-center bg-gradient-to-br from-blue-300 via-blue-400 to-blue-500 text-gray-800">
      <motion.div
        className="text-center"
        initial={{ opacity: 0, y: -20 }}
        animate={{ opacity: 1, y: 0 }}
        transition={{ duration: 0.8 }}
      >
        <h1 className="text-5xl font-extrabold text-white mb-6 drop-shadow-lg">Dear Maddie, From Shane</h1>
        <p className="text-lg text-blue-100 mb-8">
          Please give me a bit of your time.
        </p>
      </motion.div>

      <motion.div
        initial={{ opacity: 0, scale: 0.9 }}
        animate={{ opacity: 1, scale: 1 }}
        transition={{ duration: 0.8 }}
      >
        <Card className="p-6 max-w-md shadow-xl rounded-3xl">
          <CardContent className="text-center">
            <p className="mb-4">Click me</p>
            <Button
              onClick={navigateToLetter}
              className="bg-blue-600 text-white hover:bg-blue-800 transition py-3 px-6 rounded-xl"
            >
              Read the Letter
            </Button>
          </CardContent>
        </Card>
      </motion.div>

      <motion.div
        className="mt-8 text-center"
        initial={{ opacity: 0, y: 20 }}
        animate={{ opacity: 1, y: 0 }}
        transition={{ duration: 0.8, delay: 0.5 }}
      >
        <p className="mb-4 text-blue-200">
          When you're ready, click the button below to hear how I truly feel.
        </p>
        <Button
          onClick={navigateToSong}
          className="bg-red-500 text-white hover:bg-red-700 transition py-3 px-6 rounded-xl"
        >
          You Belong With Me 🎵
        </Button>
      </motion.div>

      <motion.div
        className="mt-12 text-center"
        initial={{ opacity: 0, y: 20 }}
        animate={{ opacity: 1, y: 0 }}
        transition={{ duration: 1 }}
      >
        <div className="flex justify-center items-center space-x-6">
          <img
            src="https://files.worldwildlife.org/wwfcmsprod/images/HERO_Red_Panda_279141/hero_full/7bkg4jrmln_XL_279141.jpg"
            alt="Red Panda"
            className="w-24 h-24 rounded-full shadow-lg"
          />
          <img
            src="https://giraffeconservation.org/wp-content/uploads/2024/11/featured-16-9_nubian-10-topaz.jpg"
            alt="Giraffe"
            className="w-24 h-24 rounded-full shadow-lg"
          />
        </div>
        <p className="mt-6 text-white font-semibold">
          I love you like you love red pandas and giraffes. 🦒🐾
        </p>
      </motion.div>
    </div>
  );
}
