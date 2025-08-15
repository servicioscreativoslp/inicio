# inicio
inicio
import React from "react";
import { motion } from "framer-motion";
import { Button } from "@/components/ui/button";
import { Card, CardContent, CardHeader, CardTitle } from "@/components/ui/card";
import { Badge } from "@/components/ui/badge";
import { CheckCircle2, Instagram, Mail, Phone, Rocket, Sparkles, Layers, PenTool, Presentation, Palette, Camera, Wrench } from "lucide-react";

// Single-file, modern one-page website for a creative services studio.
// Tailwind is assumed available by the canvas. All copy is in Spanish.
// Replace placeholders (email, teléfono, portfolio) with real data when ready.

export default function Website() {
  const navItems = [
    { id: "servicios", label: "Servicios" },
    { id: "portfolio", label: "Portfolio" },
    { id: "nosotros", label: "Nosotros" },
    { id: "contacto", label: "Contacto" },
  ];

  const servicios = [
    {
      icon: <PenTool className="w-6 h-6" aria-hidden />,
      title: "Diseño de CV & Presentaciones",
      desc: "Currículums profesionales y presentaciones que venden tus ideas.",
    },
    {
      icon: <Presentation className="w-6 h-6" aria-hidden />,
      title: "Presentaciones PowerPoint / Canva",
      desc: "Diapositivas claras, visuales y listas para impactar.",
    },
    {
      icon: <Palette className="w-6 h-6" aria-hidden />,
      title: "Identidad & Branding",
      desc: "Logotipos, paletas y manuales básicos para tu marca.",
    },
    {
      icon: <Layers className="w-6 h-6" aria-hidden />,
      title: "Social Media & Flyers",
      desc: "Piezas para Instagram y promos impresas listas para producción.",
    },
    {
      icon: <Camera className="w-6 h-6" aria-hidden />,
      title: "Retoque & Fotoproducto",
      desc: "Edición, recorte y mejora de fotos de productos.",
    },
    {
      icon: <Wrench className="w-6 h-6" aria-hidden />,
      title: "Soporte Creativo On‑Demand",
      desc: "Pequeños ajustes, exportaciones y formatos cuando los necesites.",
    },
  ];

  const portfolio = [
    {
      title: "CV Profesional Minimalista",
      tag: "CV / Rebranding",
    },
    {
      title: "Pitch Deck Comercial",
      tag: "Presentación",
    },
    {
      title: "Identidad Express",
      tag: "Branding",
    },
    {
      title: "Pack de Historias IG",
      tag: "Social Media",
    },
    {
      title: "Catálogo A4 – Productos",
      tag: "Editorial",
    },
    {
      title: "Flyer Promocional",
      tag: "Impreso",
    },
  ];

  return (
    <div className="min-h-screen bg-gradient-to-b from-white to-slate-50 text-slate-800">
      {/* Navbar */}
      <header className="sticky top-0 z-40 bg-white/70 backdrop-blur border-b border-slate-200">
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-16 flex items-center justify-between">
          <a href="#" className="flex items-center gap-2 font-semibold text-slate-900">
            <Sparkles className="w-5 h-5" />
            <span>Servicios Creativos LP</span>
            <Badge className="ml-2" variant="secondary">Estudio</Badge>
          </a>
          <nav className="hidden md:flex items-center gap-6">
            {navItems.map((n) => (
              <a key={n.id} href={`#${n.id}`} className="text-sm hover:text-slate-950 transition-colors">
                {n.label}
              </a>
            ))}
            <a
              href="https://www.instagram.com/servicios.creativos.lp/"
              target="_blank"
              rel="noreferrer"
              className="inline-flex items-center gap-2 text-sm px-3 py-2 rounded-2xl border border-slate-300 hover:bg-slate-100"
            >
              <Instagram className="w-4 h-4" /> Instagram
            </a>
          </nav>
          <div className="md:hidden">
            <a
              href="#contacto"
              className="text-sm px-3 py-2 rounded-2xl border border-slate-300 hover:bg-slate-100"
            >Contacto</a>
          </div>
        </div>
      </header>

      {/* Hero */}
      <section className="relative overflow-hidden">
        <div className="absolute inset-0 -z-10 opacity-30 bg-[radial-gradient(ellipse_at_top,_var(--tw-gradient-stops))] from-indigo-200 via-sky-200 to-transparent"></div>
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-20">
          <motion.div initial={{ opacity: 0, y: 20 }} animate={{ opacity: 1, y: 0 }} transition={{ duration: 0.6 }} className="grid md:grid-cols-2 gap-10 items-center">
            <div>
              <Badge className="mb-4" variant="secondary">Diseño rápido y profesional</Badge>
              <h1 className="text-4xl/tight md:text-5xl font-extrabold tracking-tight text-slate-900">
                Tu imagen, <span className="bg-clip-text text-transparent bg-gradient-to-r from-indigo-600 to-sky-500">bien diseñada</span>.
              </h1>
              <p className="mt-4 text-slate-600 max-w-prose">
                Creamos CV, presentaciones, identidades y piezas para redes que elevan tu marca. Atención ágil, resultados prolijos y entregas listas para usar.
              </p>
              <div className="mt-6 flex flex-wrap gap-3">
                <Button asChild className="rounded-2xl px-5">
                  <a href="#contacto"><Rocket className="w-4 h-4 mr-2" />Pedir presupuesto</a>
                </Button>
                <Button asChild variant="secondary" className="rounded-2xl px-5">
                  <a href="https://www.instagram.com/servicios.creativos.lp/" target="_blank" rel="noreferrer">
                    <Instagram className="w-4 h-4 mr-2" /> Ver trabajos en Instagram
                  </a>
                </Button>
              </div>
              <ul className="mt-6 grid sm:grid-cols-3 gap-2 text-sm text-slate-600">
                {[
                  "Entrega en formatos editables",
                  "Archivo listo para impresión",
                  "Soporte y ajustes menores incluidos",
                ].map((t) => (
                  <li key={t} className="flex items-center gap-2"><CheckCircle2 className="w-4 h-4" /> {t}</li>
                ))}
              </ul>
            </div>
            <div>
              <motion.div initial={{ opacity: 0, scale: 0.95 }} animate={{ opacity: 1, scale: 1 }} transition={{ delay: 0.15, duration: 0.6 }} className="relative">
                <div className="aspect-[4/3] rounded-3xl border border-slate-200 bg-gradient-to-br from-white to-slate-100 shadow-sm grid place-items-center">
                  <div className="text-center p-8">
                    <h3 className="text-xl font-semibold">Muestra de piezas</h3>
                    <p className="text-slate-600 mt-2">Reemplazá este bloque con capturas reales de tus trabajos.</p>
                    <div className="mt-4 grid grid-cols-3 gap-2">
                      {Array.from({ length: 6 }).map((_, i) => (
                        <div key={i} className="aspect-square rounded-xl bg-slate-200" />
                      ))}
                    </div>
                  </div>
                </div>
              </motion.div>
            </div>
          </motion.div>
        </div>
      </section>

      {/* Servicios */}
      <section id="servicios" className="py-16">
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
          <div className="flex items-end justify-between mb-8">
            <h2 className="text-2xl md:text-3xl font-bold">Servicios</h2>
            <p className="text-slate-600 text-sm">Elegí el servicio que necesitás, nosotros lo resolvemos.</p>
          </div>
          <div className="grid md:grid-cols-2 lg:grid-cols-3 gap-6">
            {servicios.map((s) => (
              <Card key={s.title} className="rounded-2xl">
                <CardHeader className="flex flex-row items-center gap-3 pb-2">
                  <div className="p-2 rounded-xl bg-slate-100 border">{s.icon}</div>
                  <CardTitle className="text-base">{s.title}</CardTitle>
                </CardHeader>
                <CardContent>
                  <p className="text-sm text-slate-600">{s.desc}</p>
                </CardContent>
              </Card>
            ))}
          </div>
        </div>
      </section>

      {/* Portfolio */}
      <section id="portfolio" className="py-16 bg-white">
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
          <div className="flex items-end justify-between mb-8">
            <h2 className="text-2xl md:text-3xl font-bold">Portfolio</h2>
            <p className="text-slate-600 text-sm">Un vistazo a trabajos recientes.</p>
          </div>
          <div className="grid sm:grid-cols-2 lg:grid-cols-3 gap-6">
            {portfolio.map((p) => (
              <Card key={p.title} className="rounded-2xl overflow-hidden">
                <div className="aspect-[4/3] bg-slate-200" />
                <CardHeader>
                  <CardTitle className="text-base flex items-center justify-between">
                    {p.title}
                    <Badge variant="secondary">{p.tag}</Badge>
                  </CardTitle>
                </CardHeader>
              </Card>
            ))}
          </div>
        </div>
      </section>

      {/* Nosotros */}
      <section id="nosotros" className="py-16">
        <div className="max-w-5xl mx-auto px-4 sm:px-6 lg:px-8">
          <div className="grid md:grid-cols-2 gap-10 items-center">
            <div>
              <h2 className="text-2xl md:text-3xl font-bold">Sobre el estudio</h2>
              <p className="mt-4 text-slate-600">
                Somos un pequeño equipo creativo enfocado en resolver rápido y bien. Nos especializamos en piezas para comunicar y vender: CV, presentaciones, identidad, flyers y catálogos. Trabajamos 100% online y entregamos archivos editables y listos para impresión.
              </p>
              <ul className="mt-6 space-y-2 text-slate-700 text-sm">
                <li className="flex items-center gap-2"><CheckCircle2 className="w-4 h-4" /> Atención personalizada</li>
                <li className="flex items-center gap-2"><CheckCircle2 className="w-4 h-4" /> Entregas en tiempo y forma</li>
                <li className="flex items-center gap-2"><CheckCircle2 className="w-4 h-4" /> Revisión y ajustes menores incluidos</li>
              </ul>
            </div>
            <div>
              <div className="rounded-3xl border border-slate-200 bg-white p-6 shadow-sm">
                <h3 className="font-semibold">Cómo trabajamos</h3>
                <ol className="mt-4 space-y-3 text-sm text-slate-700">
                  <li><strong>1. Brief simple:</strong> Nos contás qué necesitás y referencias.</li>
                  <li><strong>2. Propuesta:</strong> Enviamos timing y costo.</li>
                  <li><strong>3. Diseño:</strong> Iteramos con tus comentarios.</li>
                  <li><strong>4. Entrega:</strong> Archivos finales + editables.</li>
                </ol>
              </div>
            </div>
          </div>
        </div>
      </section>

      {/* Contacto */}
      <section id="contacto" className="py-16 bg-white">
        <div className="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
          <div className="text-center max-w-2xl mx-auto">
            <h2 className="text-2xl md:text-3xl font-bold">Contactanos</h2>
            <p className="mt-3 text-slate-600">Pedí tu presupuesto sin compromiso. Respondemos rápido.</p>
          </div>

          <div className="mt-8 grid md:grid-cols-2 gap-6">
            <Card className="rounded-2xl">
              <CardHeader>
                <CardTitle className="text-base">Escribinos</CardTitle>
              </CardHeader>
              <CardContent>
                <form className="space-y-3" action="mailto:tu-email@ejemplo.com" method="post" encType="text/plain">
                  <div>
                    <label className="text-sm">Nombre</label>
                    <input name="nombre" className="mt-1 w-full rounded-xl border border-slate-300 p-2" placeholder="Tu nombre" />
                  </div>
                  <div>
                    <label className="text-sm">Email</label>
                    <input name="email" type="email" className="mt-1 w-full rounded-xl border border-slate-300 p-2" placeholder="tu@correo.com" />
                  </div>
                  <div>
                    <label className="text-sm">Mensaje</label>
                    <textarea name="mensaje" className="mt-1 w-full rounded-xl border border-slate-300 p-2 h-28" placeholder="Contanos qué necesitás"></textarea>
                  </div>
                  <Button type="submit" className="rounded-2xl">Enviar consulta</Button>
                </form>
              </CardContent>
            </Card>

            <Card className="rounded-2xl">
              <CardHeader>
                <CardTitle className="text-base">Datos de contacto</CardTitle>
              </CardHeader>
              <CardContent>
                <ul className="space-y-3 text-sm text-slate-700">
                  <li className="flex items-center gap-2"><Mail className="w-4 h-4" /> tu-email@ejemplo.com</li>
                  <li className="flex items-center gap-2"><Phone className="w-4 h-4" /> +54 9 0000 0000</li>
                  <li className="flex items-center gap-2"><Instagram className="w-4 h-4" />
                    <a className="underline" href="https://www.instagram.com/servicios.creativos.lp/" target="_blank" rel="noreferrer">@servicios.creativos.lp</a>
                  </li>
                </ul>
                <div className="mt-4">
                  <Button asChild variant="secondary" className="rounded-2xl w-full">
                    <a href="https://www.instagram.com/servicios.creativos.lp/" target="_blank" rel="noreferrer" className="flex items-center justify-center gap-2">
                      <Instagram className="w-4 h-4" /> Escribir por Instagram
                    </a>
                  </Button>
                </div>
              </CardContent>
            </Card>
          </div>
        </div>
      </section>

      {/* Footer */}
      <footer className="py-10">
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-sm text-slate-600">
          <div className="flex flex-col md:flex-row items-center justify-between gap-4">
            <p>© {new Date().getFullYear()} Servicios Creativos LP. Todos los derechos reservados.</p>
            <div className="flex items-center gap-3">
              <a href="#" className="hover:underline">Términos</a>
              <span>•</span>
              <a href="#" className="hover:underline">Privacidad</a>
            </div>
          </div>
        </div>
      </footer>
    </div>
  );
}
