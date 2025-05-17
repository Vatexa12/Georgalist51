// მთავარი ფაილი: App.jsx
import React from "react";
import { BrowserRouter as Router, Routes, Route, Link } from "react-router-dom";
import Home from "./pages/Home";
import About from "./pages/About";
import Vision from "./pages/Vision";
import Blog from "./pages/Blog";
import Join from "./pages/Join";
import Donate from "./pages/Donate";
import Contact from "./pages/Contact";
import logo from "./assets/logo.png";

function App() {
  return (
    <Router>
      <div className="min-h-screen bg-red-900 text-white">
        <header className="flex items-center justify-between px-6 py-4 shadow-md bg-red-950">
          <img src={logo} alt="ლოგო" className="h-14" />
          <nav className="space-x-4 text-lg">
            <Link to="/">მთავარი</Link>
            <Link to="/about">ჩვენ შესახებ</Link>
            <Link to="/vision">პროგრამა</Link>
            <Link to="/blog">სიახლეები</Link>
            <Link to="/join">შემოგვიერთდი</Link>
            <Link to="/donate">დონაციები</Link>
            <Link to="/contact">კონტაქტი</Link>
          </nav>
        </header>

        <main className="p-6">
          <Routes>
            <Route path="/" element={<Home />} />
            <Route path="/about" element={<About />} />
            <Route path="/vision" element={<Vision />} />
            <Route path="/blog" element={<Blog />} />
            <Route path="/join" element={<Join />} />
            <Route path="/donate" element={<Donate />} />
            <Route path="/contact" element={<Contact />} />
          </Routes>
        </main>

        <footer className="text-center py-4 border-t border-white/20 text-sm">
          &copy; 2025 ქართველისტები. ყველა უფლება დაცულია.
        </footer>
      </div>
    </Router>
  );
}

export default App;

// გვერდი: About.jsx
// ფაილი მდებარეობს: ./pages/About.jsx
import React from "react";

function About() {
  return (
    <div className="max-w-4xl mx-auto space-y-6">
      <h1 className="text-3xl font-bold">ჩვენ შესახებ</h1>
      <p className="text-lg">
        გეორგალისტები — ახალი მემარჯვენე, პოპულისტური, ნაციონალ-კონსერვატიული პოლიტიკური გაერთიანებაა,
        რომლის მთავარი მიზანია საქართველოს ერთიანობის დაცვა და ეროვნული გადარჩენა.
      </p>
      <p className="text-lg">
        ჩვენი იდეოლოგია ეფუძნება ტრადიციებზე, ქრისტიანულ ღირებულებებზე, ეროვნულ სუვერენიტეტზე და ეკონომიკურ თავისუფლებაზე.
        ჩვენ გვჯერა, რომ საქართველოს მომავალი დამოკიდებულია მტკიცე იდენტობასა და გაბედულ ლიდერობაზე.
      </p>
      <p className="text-lg font-semibold text-yellow-300">
        დაგვიდექით გვერდში — ერთად გადავარჩინოთ ჩვენი სამშობლო!
      </p>
    </div>
  );
}

export default About;

