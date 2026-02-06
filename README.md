import { motion } from "framer-motion";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { Github, Linkedin, Mail } from "lucide-react";

export default function Portfolio() {
  const skills = {
    languages: ["Java", "JavaScript", "React", "C#", "C++", "PHP", "IoT"],
    frontend: ["HTML5", "CSS3", "Material UI"],
    tools: ["MySQL", "Firebase", "Git"],
  };

  const projects = [
    {
      title: "Enrollment System",
      date: "09/2024 – 11/2024",
      description:
        "A comprehensive enrollment system developed using ASP.NET with Razor Pages and SQL Server for secure and reliable data management.",
    },
    {
      title: "Boy Cabbage Web Game",
      date: "01/2023 – 05/2023",
      description:
        "A 2D platform web game where players guide a character through levels filled with challenges, obstacles, and enemies.",
    },
    {
      title: "JobFilter",
      date: "08/2025 – 12/2025",
      description:
        "A PHP-based job matching platform that connects job seekers with relevant job listings based on skills, experience, and preferences.",
    },
    {
      title: "Cuppa: Your Coffee, Your Way",
      date: "08/2025 – 12/2025",
      description:
        "An IoT-enabled smart coffee brewing system with Android integration for remote brewing, scheduling, and real-time alerts.",
    },
  ];

  return (
    <div className="min-h-screen bg-slate-50 text-slate-800">
      {/* Hero */}
      <section className="max-w-6xl mx-auto px-6 py-20">
        <motion.div
          initial={{ opacity: 0, y: 20 }}
          animate={{ opacity: 1, y: 0 }}
          transition={{ duration: 0.6 }}
          className="grid md:grid-cols-2 gap-10 items-center"
        >
          <div>
            <h1 className="text-4xl md:text-5xl font-bold mb-4">
              Frank Oliver Narag Bentoy
            </h1>
            <p className="text-lg font-medium text-slate-600 mb-4">
              Web Developer
            </p>
            <p className="text-base text-slate-600 mb-6">
              I am a dedicated Web Developer with a strong background in programming. I specialize in building efficient and scalable applications using ASP.NET, Razor Pages, and database-driven systems. I enjoy learning new technologies and creating solutions that make a real-world impact.
            </p>
            <div className="flex gap-3">
              <Button asChild>
                <a href="mailto:frankoliverbentoy@gmail.com">
                  <Mail className="w-4 h-4 mr-2" /> Contact Me
                </a>
              </Button>
              <Button variant="outline" asChild>
                <a href="https://github.com/FRC_FRANKY" target="_blank">
                  <Github className="w-4 h-4 mr-2" /> GitHub
                </a>
              </Button>
              <Button variant="outline" asChild>
                <a
                  href="https://www.linkedin.com/in/frank-oliver-bentoy-33b116238"
                  target="_blank"
                >
                  <Linkedin className="w-4 h-4 mr-2" /> LinkedIn
                </a>
              </Button>
            </div>
          </div>
        </motion.div>
      </section>

      {/* About */}
      <section className="bg-white py-16">
        <div className="max-w-6xl mx-auto px-6">
          <h2 className="text-2xl font-semibold mb-6">About Me</h2>
          <p className="text-slate-600 leading-relaxed">
            I am currently taking Bachelor of Science in Information Technology at the University of Cebu – Banilad. I have experience working on academic and personal projects such as web systems, games, and IoT applications. My main focus is backend and full‑stack web development, particularly using ASP.NET and database technologies.
          </p>
        </div>
      </section>

      {/* Skills */}
      <section className="py-16">
        <div className="max-w-6xl mx-auto px-6">
          <h2 className="text-2xl font-semibold mb-8">Technical Skills</h2>
          <div className="grid md:grid-cols-3 gap-6">
            <Card className="rounded-2xl shadow-sm">
              <CardContent className="p-6">
                <h3 className="font-semibold mb-3">Languages & Frameworks</h3>
                <ul className="space-y-1 text-slate-600">
                  {skills.languages.map((s) => (
                    <li key={s}>• {s}</li>
                  ))}
                </ul>
              </CardContent>
            </Card>

            <Card className="rounded-2xl shadow-sm">
              <CardContent className="p-6">
                <h3 className="font-semibold mb-3">Frontend & UI</h3>
                <ul className="space-y-1 text-slate-600">
                  {skills.frontend.map((s) => (
                    <li key={s}>• {s}</li>
                  ))}
                </ul>
              </CardContent>
            </Card>

            <Card className="rounded-2xl shadow-sm">
              <CardContent className="p-6">
                <h3 className="font-semibold mb-3">Databases, Cloud & Tools</h3>
                <ul className="space-y-1 text-slate-600">
                  {skills.tools.map((s) => (
                    <li key={s}>• {s}</li>
                  ))}
                </ul>
              </CardContent>
            </Card>
          </div>
        </div>
      </section>

      {/* Projects */}
      <section className="bg-white py-16">
        <div className="max-w-6xl mx-auto px-6">
          <h2 className="text-2xl font-semibold mb-8">Projects</h2>
          <div className="grid md:grid-cols-2 gap-6">
            {projects.map((project) => (
              <Card key={project.title} className="rounded-2xl shadow-sm">
                <CardContent className="p-6">
                  <h3 className="font-semibold text-lg mb-1">
                    {project.title}
                  </h3>
                  <p className="text-sm text-slate-500 mb-3">
                    {project.date}
                  </p>
                  <p className="text-slate-600">{project.description}</p>
                </CardContent>
              </Card>
            ))}
          </div>
        </div>
      </section>

      {/* Education & Experience */}
      <section className="py-16">
        <div className="max-w-6xl mx-auto px-6 grid md:grid-cols-2 gap-10">
          <div>
            <h2 className="text-2xl font-semibold mb-4">Education</h2>
            <p className="font-medium">Bachelor of Science in Information Technology</p>
            <p className="text-slate-600">University of Cebu – Banilad</p>
            <p className="text-slate-500">2021 – Present</p>
          </div>

          <div>
            <h2 className="text-2xl font-semibold mb-4">Experience</h2>
            <p className="font-medium">Project Manager – School Project</p>
            <p className="text-slate-600">September 2024 – December 2024</p>
            <p className="text-slate-600 mt-2">
              Worked with a development team on web-based projects using ASP.NET, SQL Server, and MySQL while helping manage tasks and timelines.
            </p>
          </div>
        </div>
      </section>

      {/* Footer */}
      <footer className="bg-slate-900 text-white py-10">
        <div className="max-w-6xl mx-auto px-6 text-center space-y-2">
          <p className="font-semibold">Frank Oliver Narag Bentoy</p>
          <p className="text-sm">Cebu, Philippines</p>
          <p className="text-sm">frankoliverbentoy@gmail.com | +63 956 077 2456</p>
        </div>
      </footer>
    </div>
  );
}
