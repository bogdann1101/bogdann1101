import { useState } from "react";
import { motion } from "framer-motion";

export default function App() {
  const [size, setSize] = useState(1);

  return (
    <div className="flex flex-col items-center justify-center min-h-screen bg-gray-100">
      <motion.h1
        className="text-3xl font-bold mb-6"
        animate={{ scale: [1, 1.2, 1] }}
        transition={{ repeat: Infinity, duration: 1.5 }}
      >
        Îmi puneți un 10?
      </motion.h1>
      <motion.div
        className="text-green-500 text-6xl font-bold mb-6"
        animate={{ scale: [1, 1.5, 1] }}
        transition={{ repeat: Infinity, duration: 2 }}
      >
        10
      </motion.div>
      <div className="flex gap-4">
        <motion.button
          className="bg-green-500 text-white px-6 py-3 rounded-lg text-xl"
          style={{ transform: `scale(${size})` }}
        >
          Da
        </motion.button>
        <button
          className="bg-red-500 text-white px-6 py-3 rounded-lg text-xl"
          onClick={() => setSize(size * 1.3)}
        >
          Nu
        </button>
      </div>
    </div>
  );
}

