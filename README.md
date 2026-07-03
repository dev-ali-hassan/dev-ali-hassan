<p align="center">
  <img
    src="ChatGPT Image Jul 3, 2026, 05_43_49 AM.png"
    alt="Ali Hassan - Full Stack Developer"
    width="100%"
  />
</p>

<h2 align="center">🌌 Who Am I ?</h2>

<p align="center">
  Full Stack Developer passionate about creating modern web, mobile, and desktop applications with performance, scalability, and exceptional user experiences in mind.
</p>
<br />
import {
  FaReact,
  FaNodeJs,
  FaGitAlt,
  FaGithub,
  FaPhp,
} from "react-icons/fa";

import {
  SiTypescript,
  SiJavascript,
  SiHtml5,
  SiCss3,
  SiTailwindcss,
  SiExpress,
  SiMysql,
  SiVisualstudiocode,
  SiVite,
} from "react-icons/si";

const frontend = [
  { icon: <FaReact />, name: "React", color: "text-cyan-400" },
  { icon: <SiTypescript />, name: "TypeScript", color: "text-blue-500" },
  { icon: <SiJavascript />, name: "JavaScript", color: "text-yellow-400" },
  { icon: <SiHtml5 />, name: "HTML5", color: "text-orange-500" },
  { icon: <SiCss3 />, name: "CSS3", color: "text-blue-400" },
  { icon: <SiTailwindcss />, name: "Tailwind", color: "text-cyan-300" },
];

const backend = [
  { icon: <FaNodeJs />, name: "Node.js", color: "text-green-500" },
  { icon: <SiExpress />, name: "Express", color: "text-gray-300" },
  { icon: <FaPhp />, name: "PHP", color: "text-indigo-300" },
  { icon: <SiMysql />, name: "MySQL", color: "text-sky-500" },
];

const tools = [
  { icon: <FaGitAlt />, name: "Git", color: "text-orange-500" },
  { icon: <FaGithub />, name: "GitHub", color: "text-white" },
  { icon: <SiVisualstudiocode />, name: "VS Code", color: "text-blue-500" },
  { icon: <SiVite />, name: "Vite", color: "text-violet-400" },
];

const Row = ({ title, items }) => (
  <div className="flex flex-col md:flex-row md:items-start gap-8">
    {/* Left Heading */}
    <div className="w-32">
      <h3 className="text-purple-400 font-bold uppercase tracking-wider text-sm">
        {title}
      </h3>
    </div>

    {/* Icons */}
    <div className="flex flex-wrap gap-8">
      {items.map((item) => (
        <div
          key={item.name}
          className="flex flex-col items-center"
        >
          <div className="w-16 h-16 rounded-xl bg-slate-800 flex items-center justify-center shadow-md hover:scale-105 transition">
            <span className={`text-4xl ${item.color}`}>
              {item.icon}
            </span>
          </div>

          <p className="mt-2 text-sm text-gray-300">
            {item.name}
          </p>
        </div>
      ))}
    </div>
  </div>
);

export default function TechStack() {
  return (
    <section className="max-w-6xl mx-auto py-16 px-6">
      <h2 className="flex items-center gap-3 text-4xl font-bold text-white mb-12">
        <span className="text-purple-500">&lt;/&gt;</span>
        <span>TECH STACK</span>
      </h2>

      <div className="space-y-12">
        <Row title="FRONTEND" items={frontend} />
        <Row title="BACKEND" items={backend} />
        <Row title="TOOLS" items={tools} />
      </div>
    </section>
  );
}
