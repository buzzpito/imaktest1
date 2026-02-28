import { useState, useEffect, useMemo } from "react";
import { LineChart, Line, XAxis, YAxis, CartesianGrid, Tooltip, ResponsiveContainer, PieChart, Pie, Cell, Legend } from "recharts";

// ─── GOOGLE FONTS ────────────────────────────────────────────────────────────
const fontLink = document.createElement("link");
fontLink.rel = "stylesheet";
fontLink.href = "https://fonts.googleapis.com/css2?family=Barlow+Condensed:wght@500;600;700&family=DM+Sans:wght@300;400;500;600&display=swap";
document.head.appendChild(fontLink);

const style = document.createElement("style");
style.textContent = `
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
  body { font-family: 'DM Sans', sans-serif; background: #0f1117; }
  :root {
    --navy: #0f1117;
    --navy2: #161b27;
    --navy3: #1e2535;
    --border: #2a3348;
    --text: #e8eaf0;
    --muted: #7a8499;
    --orange: #f5820a;
    --orange2: #ff9d38;
    --green: #22c55e;
    --red: #ef4444;
    --blue: #3b82f6;
    --yellow: #eab308;
  }
  h1,h2,h3,h4,h5 { font-family: 'Barlow Condensed', sans-serif; letter-spacing: 0.02em; }
  ::-webkit-scrollbar { width: 4px; height: 4px; }
  ::-webkit-scrollbar-track { background: var(--navy2); }
  ::-webkit-scrollbar-thumb { background: var(--border); border-radius: 2px; }
  .fade-in { animation: fadeIn 0.25s ease; }
  @keyframes fadeIn { from { opacity:0; transform:translateY(6px); } to { opacity:1; transform:translateY(0); } }
  .btn { display:inline-flex; align-items:center; gap:6px; padding:8px 16px; border-radius:6px; font-family:'DM Sans',sans-serif; font-size:13px; font-weight:500; cursor:pointer; border:none; transition:all 0.15s; }
  .btn-primary { background:var(--orange); color:#fff; }
  .btn-primary:hover { background:var(--orange2); }
  .btn-secondary { background:var(--navy3); color:var(--text); border:1px solid var(--border); }
  .btn-secondary:hover { background:var(--border); }
  .btn-danger { background:#7f1d1d; color:#fca5a5; border:1px solid #991b1b; }
  .btn-danger:hover { background:#991b1b; }
  .btn-sm { padding:5px 10px; font-size:12px; }
  input, select, textarea { background:var(--navy3); border:1px solid var(--border); color:var(--text); border-radius:6px; padding:8px 12px; font-family:'DM Sans',sans-serif; font-size:13px; outline:none; transition:border 0.15s; }
  input:focus, select:focus, textarea:focus { border-color:var(--orange); }
  input::placeholder { color:var(--muted); }
  select option { background:var(--navy3); }
  table { width:100%; border-collapse:collapse; font-size:13px; }
  thead th { background:var(--navy3); color:var(--muted); font-weight:500; text-transform:uppercase; font-size:11px; letter-spacing:0.06em; padding:10px 14px; text-align:left; border-bottom:1px solid var(--border); white-space:nowrap; }
  tbody tr { border-bottom:1px solid var(--border); transition:background 0.1s; }
  tbody tr:hover { background:rgba(255,255,255,0.02); }
  tbody td { padding:10px 14px; color:var(--text); vertical-align:middle; }
  .badge { display:inline-block; padding:3px 8px; border-radius:4px; font-size:11px; font-weight:600; text-transform:uppercase; letter-spacing:0.04em; }
  .badge-livré { background:#14532d; color:#86efac; }
  .badge-confirmé { background:#1e3a5f; color:#93c5fd; }
  .badge-en-cours { background:#451a03; color:#fdba74; }
  .badge-retourné { background:#450a0a; color:#fca5a5; }
  .badge-annulé { background:#1c1917; color:#a8a29e; }
  .badge-remboursé { background:#4a1d96; color:#c4b5fd; }
  .badge-manque { background:#422006; color:#fed7aa; }
  .modal-overlay { position:fixed; inset:0; background:rgba(0,0,0,0.7); z-index:1000; display:flex; align-items:center; justify-content:center; padding:20px; }
  .modal { background:var(--navy2); border:1px solid var(--border); border-radius:12px; padding:28px; width:100%; max-width:560px; max-height:90vh; overflow-y:auto; }
  .card { background:var(--navy2); border:1px solid var(--border); border-radius:10px; padding:20px; }
  .sidebar-link { display:flex; align-items:center; gap:10px; padding:10px 14px; border-radius:8px; color:var(--muted); font-size:13px; font-weight:500; cursor:pointer; transition:all 0.15s; margin-bottom:2px; }
  .sidebar-link:hover { background:var(--navy3); color:var(--text); }
  .sidebar-link.active { background:rgba(245,130,10,0.12); color:var(--orange); border-left:2px solid var(--orange); }
  .kpi-card { background:var(--navy2); border:1px solid var(--border); border-radius:10px; padding:20px 24px; position:relative; overflow:hidden; }
  .kpi-card::before { content:''; position:absolute; top:0; right:0; width:80px; height:80px; border-radius:0 10px 0 80px; opacity:0.06; }
  .label { display:block; font-size:11px; text-transform:uppercase; letter-spacing:0.06em; color:var(--muted); font-weight:600; margin-bottom:4px; }
  .form-group { margin-bottom:16px; }
  .form-group label { display:block; font-size:12px; color:var(--muted); margin-bottom:6px; font-weight:500; text-transform:uppercase; letter-spacing:0.05em; }
  .form-row { display:grid; grid-template-columns:1fr 1fr; gap:12px; }
  @media(max-width:768px) { .form-row { grid-template-columns:1fr; } }
  .tab { padding:8px 16px; border-radius:6px; cursor:pointer; font-size:13px; font-weight:500; color:var(--muted); transition:all 0.15s; border:1px solid transparent; }
  .tab.active { background:var(--navy3); color:var(--text); border-color:var(--border); }
  .checkbox-custom { width:16px; height:16px; accent-color:var(--orange); cursor:pointer; }
  .print-only { display:none; }
  @media print {
    .no-print { display:none !important; }
    .print-only { display:block; }
    body { background:white; }
  }
`;
document.head.appendChild(style);

// ─── MOCK DATA ────────────────────────────────────────────────────────────────
const STATUTS = ["Confirmé","En cours","Livré","Retourné","Annulé","Manque de stock","Remboursé"];
const VILLES = ["Casablanca","Rabat","Marrakech","Fès","Agadir","Tanger","Meknès","Oujda","Kenitra","Tétouan"];
const PRODUITS = ["AirPods Pro","Montre connectée","Sac cuir","Parfum Oud","Écouteurs BT","Chargeur rapide","Ceinture sport","Lunettes soleil"];

function genId() { return Math.random().toString(36).substr(2,8).toUpperCase(); }
function randomDate(daysBack) {
  const d = new Date(); d.setDate(d.getDate() - Math.floor(Math.random()*daysBack));
  return d.toISOString().split('T')[0];
}
function pick(arr) { return arr[Math.floor(Math.random()*arr.length)]; }

const MOCK_COMMANDES = Array.from({length:48}, (_,i) => ({
  id: genId(),
  client_nom: ["Mohammed Alami","Fatima Zahra","Karim Benali","Samira Tazi","Omar Idrissi","Nadia Cherkaoui","Younes Brahim","Leila Mansouri","Hassan Ouali","Asmae Berrada"][i%10],
  telephone: `06${String(Math.floor(Math.random()*99999999)).padStart(8,'0')}`,
  adresse: `${Math.floor(Math.random()*200)+1} Rue ${["Hassan II","Mohammed V","Atlas","Almohades","Liberté"][i%5]}`,
  ville: pick(VILLES),
  produit: pick(PRODUITS),
  prix: [199,249,349,199,149,99,89,179][i%8],
  frais_livraison: [20,25,30,35][i%4],
  statut: pick(STATUTS),
  agent_id: ["agent1","agent2","agent3"][i%3],
  agent_nom: ["Hamid R.","Sara K.","Younes M."][i%3],
  date_confirmation: randomDate(30),
  created_at: randomDate(30),
}));

const MOCK_USERS = [
  { id:"u1", name:"Super Admin", email:"admin@imak.ma", role:"super_admin", permissions:["dashboard","shipping","shipping_mark","facturation","access"] },
  { id:"u2", name:"Hamid Rami", email:"hamid@imak.ma", role:"agent", permissions:["dashboard","shipping","shipping_mark"] },
  { id:"u3", name:"Sara Kettani", email:"sara@imak.ma", role:"agent", permissions:["dashboard","shipping"] },
];

// ─── HELPERS ─────────────────────────────────────────────────────────────────
const badgeClass = (s) => {
  const map = { "Livré":"badge-livré","Confirmé":"badge-confirmé","En cours":"badge-en-cours","Retourné":"badge-retourné","Annulé":"badge-annulé","Remboursé":"badge-remboursé","Manque de stock":"badge-manque" };
  return `badge ${map[s]||"badge-annulé"}`;
};

const fmtMAD = (n) => `${Number(n).toLocaleString('fr-MA')} MAD`;

function getWeekRange(date = new Date()) {
  const d = new Date(date);
  const day = d.getDay(); const diff = d.getDate() - day + (day===0?-6:1);
  const mon = new Date(d.setDate(diff)); mon.setHours(0,0,0,0);
  const sun = new Date(mon); sun.setDate(mon.getDate()+6); sun.setHours(23,59,59,999);
  return { start: mon.toISOString().split('T')[0], end: sun.toISOString().split('T')[0] };
}

// ─── ICONS ───────────────────────────────────────────────────────────────────
const Icon = ({ name, size=16 }) => {
  const icons = {
    dashboard: <svg width={size} height={size} fill="none" viewBox="0 0 24 24" stroke="currentColor" strokeWidth={2}><rect x="3" y="3" width="7" height="7" rx="1"/><rect x="14" y="3" width="7" height="7" rx="1"/><rect x="3" y="14" width="7" height="7" rx="1"/><rect x="14" y="14" width="7" height="7" rx="1"/></svg>,
    shipping: <svg width={size} height={size} fill="none" viewBox="0 0 24 24" stroke="currentColor" strokeWidth={2}><path d="M5 17H3a2 2 0 01-2-2V5a2 2 0 012-2h11a2 2 0 012 2v3"/><rect x="9" y="11" width="14" height="10" rx="1"/><circle cx="12" cy="21" r="1"/><circle cx="20" cy="21" r="1"/></svg>,
    label: <svg width={size} height={size} fill="none" viewBox="0 0 24 24" stroke="currentColor" strokeWidth={2}><path d="M20.59 13.41l-7.17 7.17a2 2 0 01-2.83 0L2 12V2h10l8.59 8.59a2 2 0 010 2.82z"/><circle cx="7" cy="7" r="1.5" fill="currentColor"/></svg>,
    invoice: <svg width={size} height={size} fill="none" viewBox="0 0 24 24" stroke="currentColor" strokeWidth={2}><path d="M14 2H6a2 2 0 00-2 2v16a2 2 0 002 2h12a2 2 0 002-2V8z"/><polyline points="14 2 14 8 20 8"/><line x1="16" y1="13" x2="8" y2="13"/><line x1="16" y1="17" x2="8" y2="17"/><polyline points="10 9 9 9 8 9"/></svg>,
    users: <svg width={size} height={size} fill="none" viewBox="0 0 24 24" stroke="currentColor" strokeWidth={2}><path d="M17 21v-2a4 4 0 00-4-4H5a4 4 0 00-4 4v2"/><circle cx="9" cy="7" r="4"/><path d="M23 21v-2a4 4 0 00-3-3.87"/><path d="M16 3.13a4 4 0 010 7.75"/></svg>,
    plus: <svg width={size} height={size} fill="none" viewBox="0 0 24 24" stroke="currentColor" strokeWidth={2}><line x1="12" y1="5" x2="12" y2="19"/><line x1="5" y1="12" x2="19" y2="12"/></svg>,
    search: <svg width={size} height={size} fill="none" viewBox="0 0 24 24" stroke="currentColor" strokeWidth={2}><circle cx="11" cy="11" r="8"/><path d="M21 21l-4.35-4.35"/></svg>,
    filter: <svg width={size} height={size} fill="none" viewBox="0 0 24 24" stroke="currentColor" strokeWidth={2}><polygon points="22 3 2 3 10 12.46 10 19 14 21 14 12.46 22 3"/></svg>,
    download: <svg width={size} height={size} fill="none" viewBox="0 0 24 24" stroke="currentColor" strokeWidth={2}><path d="M21 15v4a2 2 0 01-2 2H5a2 2 0 01-2-2v-4"/><polyline points="7 10 12 15 17 10"/><line x1="12" y1="15" x2="12" y2="3"/></svg>,
    print: <svg width={size} height={size} fill="none" viewBox="0 0 24 24" stroke="currentColor" strokeWidth={2}><polyline points="6 9 6 2 18 2 18 9"/><path d="M6 18H4a2 2 0 01-2-2v-5a2 2 0 012-2h16a2 2 0 012 2v5a2 2 0 01-2 2h-2"/><rect x="6" y="14" width="12" height="8"/></svg>,
    edit: <svg width={size} height={size} fill="none" viewBox="0 0 24 24" stroke="currentColor" strokeWidth={2}><path d="M11 4H4a2 2 0 00-2 2v14a2 2 0 002 2h14a2 2 0 002-2v-7"/><path d="M18.5 2.5a2.121 2.121 0 013 3L12 15l-4 1 1-4 9.5-9.5z"/></svg>,
    trash: <svg width={size} height={size} fill="none" viewBox="0 0 24 24" stroke="currentColor" strokeWidth={2}><polyline points="3 6 5 6 21 6"/><path d="M19 6v14a2 2 0 01-2 2H7a2 2 0 01-2-2V6m3 0V4a1 1 0 011-1h4a1 1 0 011 1v2"/></svg>,
    check: <svg width={size} height={size} fill="none" viewBox="0 0 24 24" stroke="currentColor" strokeWidth={2.5}><polyline points="20 6 9 17 4 12"/></svg>,
    close: <svg width={size} height={size} fill="none" viewBox="0 0 24 24" stroke="currentColor" strokeWidth={2}><line x1="18" y1="6" x2="6" y2="18"/><line x1="6" y1="6" x2="18" y2="18"/></svg>,
    logout: <svg width={size} height={size} fill="none" viewBox="0 0 24 24" stroke="currentColor" strokeWidth={2}><path d="M9 21H5a2 2 0 01-2-2V5a2 2 0 012-2h4"/><polyline points="16 17 21 12 16 7"/><line x1="21" y1="12" x2="9" y2="12"/></svg>,
    upload: <svg width={size} height={size} fill="none" viewBox="0 0 24 24" stroke="currentColor" strokeWidth={2}><path d="M21 15v4a2 2 0 01-2 2H5a2 2 0 01-2-2v-4"/><polyline points="17 8 12 3 7 8"/><line x1="12" y1="3" x2="12" y2="15"/></svg>,
    lock: <svg width={size} height={size} fill="none" viewBox="0 0 24 24" stroke="currentColor" strokeWidth={2}><rect x="3" y="11" width="18" height="11" rx="2" ry="2"/><path d="M7 11V7a5 5 0 0110 0v4"/></svg>,
    history: <svg width={size} height={size} fill="none" viewBox="0 0 24 24" stroke="currentColor" strokeWidth={2}><polyline points="1 4 1 10 7 10"/><path d="M3.51 15a9 9 0 102.13-9.36L1 10"/></svg>,
    eye: <svg width={size} height={size} fill="none" viewBox="0 0 24 24" stroke="currentColor" strokeWidth={2}><path d="M1 12s4-8 11-8 11 8 11 8-4 8-11 8-11-8-11-8z"/><circle cx="12" cy="12" r="3"/></svg>,
  };
  return icons[name] || null;
};

// ─── LOGIN PAGE ───────────────────────────────────────────────────────────────
function LoginPage({ onLogin }) {
  const [email, setEmail] = useState("admin@imak.ma");
  const [password, setPassword] = useState("admin123");
  const [error, setError] = useState("");
  const [loading, setLoading] = useState(false);

  const handleSubmit = (e) => {
    e.preventDefault(); setLoading(true); setError("");
    setTimeout(() => {
      const user = MOCK_USERS.find(u => u.email === email);
      if (user && password === "admin123") { onLogin(user); }
      else { setError("Email ou mot de passe incorrect."); }
      setLoading(false);
    }, 600);
  };

  return (
    <div style={{ minHeight:"100vh", background:"var(--navy)", display:"flex", flexDirection:"column", alignItems:"center", justifyContent:"center", padding:"20px", position:"relative", overflow:"hidden" }}>
      {/* bg decoration */}
      <div style={{ position:"absolute", top:"-20%", right:"-10%", width:"600px", height:"600px", borderRadius:"50%", background:"radial-gradient(circle, rgba(245,130,10,0.06) 0%, transparent 70%)", pointerEvents:"none" }}/>
      <div style={{ position:"absolute", bottom:"-20%", left:"-10%", width:"400px", height:"400px", borderRadius:"50%", background:"radial-gradient(circle, rgba(59,130,246,0.05) 0%, transparent 70%)", pointerEvents:"none" }}/>
      
      <div style={{ width:"100%", maxWidth:"400px", position:"relative" }} className="fade-in">
        {/* Logo */}
        <div style={{ textAlign:"center", marginBottom:"36px" }}>
          <div style={{ display:"inline-flex", alignItems:"center", gap:"10px", marginBottom:"8px" }}>
            <div style={{ width:"40px", height:"40px", background:"var(--orange)", borderRadius:"8px", display:"flex", alignItems:"center", justifyContent:"center" }}>
              <svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="white" strokeWidth="2.5"><path d="M5 17H3a2 2 0 01-2-2V5a2 2 0 012-2h11a2 2 0 012 2v3"/><rect x="9" y="11" width="14" height="10" rx="1"/><circle cx="12" cy="21" r="1"/><circle cx="20" cy="21" r="1"/></svg>
            </div>
            <h1 style={{ fontSize:"26px", color:"var(--text)", fontWeight:700, letterSpacing:"0.03em" }}>IMAKLOGISTIC</h1>
          </div>
          <p style={{ color:"var(--muted)", fontSize:"13px" }}>Plateforme de gestion COD</p>
        </div>

        {/* Form card */}
        <div className="card" style={{ border:"1px solid var(--border)" }}>
          <h2 style={{ fontSize:"20px", color:"var(--text)", marginBottom:"6px" }}>Connexion</h2>
          <p style={{ color:"var(--muted)", fontSize:"12px", marginBottom:"24px" }}>Accès réservé aux collaborateurs autorisés</p>
          
          <form onSubmit={handleSubmit}>
            <div className="form-group">
              <label>Adresse email</label>
              <input type="email" value={email} onChange={e=>setEmail(e.target.value)} placeholder="votre@email.com" style={{ width:"100%" }} required/>
            </div>
            <div className="form-group">
              <label>Mot de passe</label>
              <input type="password" value={password} onChange={e=>setPassword(e.target.value)} placeholder="••••••••" style={{ width:"100%" }} required/>
            </div>
            {error && <div style={{ background:"#450a0a", border:"1px solid #991b1b", borderRadius:"6px", padding:"10px 12px", color:"#fca5a5", fontSize:"13px", marginBottom:"16px" }}>{error}</div>}
            <button type="submit" className="btn btn-primary" style={{ width:"100%", justifyContent:"center", padding:"11px", fontSize:"14px" }} disabled={loading}>
              {loading ? "Connexion..." : <><Icon name="lock" size={14}/> Se connecter</>}
            </button>
          </form>
          <p style={{ textAlign:"center", color:"var(--muted)", fontSize:"11px", marginTop:"16px" }}>
            Démo: admin@imak.ma / admin123
          </p>
        </div>
      </div>
    </div>
  );
}

// ─── SIDEBAR ──────────────────────────────────────────────────────────────────
const NAV_ITEMS = [
  { id:"dashboard", label:"Tableau de bord", icon:"dashboard", perm:"dashboard" },
  { id:"shipping", label:"Commandes", icon:"shipping", perm:"shipping" },
  { id:"shipping_mark", label:"Étiquettes", icon:"label", perm:"shipping_mark" },
  { id:"facturation", label:"Facturation", icon:"invoice", perm:"facturation" },
  { id:"access", label:"Accès & Utilisateurs", icon:"users", perm:"access" },
];

function Sidebar({ user, active, setActive, onLogout }) {
  const allowed = NAV_ITEMS.filter(n => user.permissions.includes(n.perm));
  return (
    <aside style={{ width:"220px", background:"var(--navy2)", borderRight:"1px solid var(--border)", height:"100vh", display:"flex", flexDirection:"column", position:"fixed", left:0, top:0, zIndex:100 }}>
      {/* Logo */}
      <div style={{ padding:"20px 16px 16px", borderBottom:"1px solid var(--border)" }}>
        <div style={{ display:"flex", alignItems:"center", gap:"8px" }}>
          <div style={{ width:"32px", height:"32px", background:"var(--orange)", borderRadius:"6px", display:"flex", alignItems:"center", justifyContent:"center", flexShrink:0 }}>
            <svg width="17" height="17" viewBox="0 0 24 24" fill="none" stroke="white" strokeWidth="2.5"><path d="M5 17H3a2 2 0 01-2-2V5a2 2 0 012-2h11a2 2 0 012 2v3"/><rect x="9" y="11" width="14" height="10" rx="1"/><circle cx="12" cy="21" r="1"/><circle cx="20" cy="21" r="1"/></svg>
          </div>
          <span style={{ fontFamily:"'Barlow Condensed',sans-serif", fontSize:"16px", fontWeight:700, color:"var(--text)", letterSpacing:"0.04em" }}>IMAKLOGISTIC</span>
        </div>
      </div>

      {/* Nav */}
      <nav style={{ flex:1, padding:"12px 8px", overflowY:"auto" }}>
        {allowed.map(item => (
          <div key={item.id} className={`sidebar-link${active===item.id?" active":""}`} onClick={()=>setActive(item.id)}>
            <Icon name={item.icon} size={15}/>
            <span>{item.label}</span>
          </div>
        ))}
      </nav>

      {/* User */}
      <div style={{ padding:"12px 8px", borderTop:"1px solid var(--border)" }}>
        <div style={{ padding:"10px 14px", background:"var(--navy3)", borderRadius:"8px", marginBottom:"8px" }}>
          <div style={{ fontSize:"13px", color:"var(--text)", fontWeight:500, marginBottom:"2px" }}>{user.name}</div>
          <div style={{ fontSize:"11px", color:"var(--orange)", textTransform:"uppercase", letterSpacing:"0.06em" }}>{user.role.replace("_"," ")}</div>
        </div>
        <button className="btn btn-secondary" style={{ width:"100%", justifyContent:"center" }} onClick={onLogout}>
          <Icon name="logout" size={13}/> Déconnexion
        </button>
      </div>
    </aside>
  );
}

// ─── DASHBOARD ────────────────────────────────────────────────────────────────
function Dashboard({ commandes }) {
  const [range, setRange] = useState("30j");
  
  const stats = useMemo(() => {
    const total = commandes.length;
    const livrees = commandes.filter(c=>c.statut==="Livré").length;
    const retournees = commandes.filter(c=>c.statut==="Retourné").length;
    const enCours = commandes.filter(c=>c.statut==="En cours").length;
    const confirmes = commandes.filter(c=>!["Annulé","Manque de stock"].includes(c.statut)).length;
    const taux = confirmes > 0 ? ((livrees/confirmes)*100).toFixed(1) : 0;
    return { total, livrees, retournees, enCours, taux };
  }, [commandes]);

  // Trend data (simulate last 7 days)
  const trendData = useMemo(() => {
    return Array.from({length:7}, (_,i) => {
      const d = new Date(); d.setDate(d.getDate()-(6-i));
      const label = d.toLocaleDateString('fr-FR',{day:'numeric',month:'short'});
      return { date:label, livrees:Math.floor(Math.random()*8)+2, enCours:Math.floor(Math.random()*5)+1, retournees:Math.floor(Math.random()*3) };
    });
  }, []);

  const pieData = [
    { name:"Livré", value:stats.livrees, color:"#22c55e" },
    { name:"En cours", value:stats.enCours, color:"#f5820a" },
    { name:"Retourné", value:stats.retournees, color:"#ef4444" },
    { name:"Autres", value:stats.total-stats.livrees-stats.enCours-stats.retournees, color:"#3b82f6" },
  ].filter(d=>d.value>0);

  const KPI = ({ label, value, sub, color }) => (
    <div className="kpi-card">
      <div className="label">{label}</div>
      <div style={{ fontSize:"32px", fontFamily:"'Barlow Condensed',sans-serif", fontWeight:700, color:color||"var(--text)", lineHeight:1.1, marginBottom:"4px" }}>{value}</div>
      {sub && <div style={{ fontSize:"11px", color:"var(--muted)" }}>{sub}</div>}
    </div>
  );

  return (
    <div className="fade-in">
      <div style={{ display:"flex", alignItems:"center", justifyContent:"space-between", marginBottom:"24px" }}>
        <div>
          <h2 style={{ fontSize:"24px", color:"var(--text)" }}>Tableau de bord</h2>
          <p style={{ color:"var(--muted)", fontSize:"13px" }}>Vue d'ensemble des opérations</p>
        </div>
        <div style={{ display:"flex", gap:"6px" }}>
          {["Aujourd'hui","7j","30j"].map(r=>(
            <div key={r} className={`tab${range===r?" active":""}`} onClick={()=>setRange(r)}>{r}</div>
          ))}
        </div>
      </div>

      {/* KPIs */}
      <div style={{ display:"grid", gridTemplateColumns:"repeat(auto-fit,minmax(180px,1fr))", gap:"14px", marginBottom:"24px" }}>
        <KPI label="Total commandes" value={stats.total} sub="Toutes périodes"/>
        <KPI label="Livrées" value={stats.livrees} color="var(--green)" sub={`+${Math.floor(stats.livrees*0.12)} cette semaine`}/>
        <KPI label="Retournées" value={stats.retournees} color="var(--red)" sub="À traiter"/>
        <KPI label="En cours" value={stats.enCours} color="var(--orange)" sub="En transit"/>
        <KPI label="Taux de livraison" value={`${stats.taux}%`} color={stats.taux>75?"var(--green)":"var(--yellow)"} sub="Sur confirmées"/>
      </div>

      {/* Charts */}
      <div style={{ display:"grid", gridTemplateColumns:"2fr 1fr", gap:"14px" }}>
        <div className="card">
          <h3 style={{ fontSize:"15px", color:"var(--text)", marginBottom:"20px" }}>Tendance des livraisons (7 derniers jours)</h3>
          <ResponsiveContainer width="100%" height={220}>
            <LineChart data={trendData} margin={{top:5,right:10,left:-20,bottom:5}}>
              <CartesianGrid strokeDasharray="3 3" stroke="#2a3348"/>
              <XAxis dataKey="date" tick={{fill:"#7a8499",fontSize:11}} axisLine={{stroke:"#2a3348"}}/>
              <YAxis tick={{fill:"#7a8499",fontSize:11}} axisLine={{stroke:"#2a3348"}}/>
              <Tooltip contentStyle={{background:"#1e2535",border:"1px solid #2a3348",borderRadius:"6px",color:"#e8eaf0",fontSize:12}}/>
              <Line type="monotone" dataKey="livrees" stroke="#22c55e" strokeWidth={2} dot={{fill:"#22c55e",r:3}} name="Livrées"/>
              <Line type="monotone" dataKey="enCours" stroke="#f5820a" strokeWidth={2} dot={{fill:"#f5820a",r:3}} name="En cours"/>
              <Line type="monotone" dataKey="retournees" stroke="#ef4444" strokeWidth={2} dot={{fill:"#ef4444",r:3}} name="Retournées"/>
            </LineChart>
          </ResponsiveContainer>
        </div>
        <div className="card">
          <h3 style={{ fontSize:"15px", color:"var(--text)", marginBottom:"20px" }}>Répartition des statuts</h3>
          <ResponsiveContainer width="100%" height={220}>
            <PieChart>
              <Pie data={pieData} cx="50%" cy="50%" innerRadius={55} outerRadius={85} paddingAngle={3} dataKey="value">
                {pieData.map((entry,i) => <Cell key={i} fill={entry.color}/>)}
              </Pie>
              <Tooltip contentStyle={{background:"#1e2535",border:"1px solid #2a3348",borderRadius:"6px",color:"#e8eaf0",fontSize:12}}/>
              <Legend formatter={(v)=><span style={{color:"var(--muted)",fontSize:11}}>{v}</span>}/>
            </PieChart>
          </ResponsiveContainer>
        </div>
      </div>

      {/* Top produits */}
      <div className="card" style={{ marginTop:"14px" }}>
        <h3 style={{ fontSize:"15px", color:"var(--text)", marginBottom:"16px" }}>Performance par produit</h3>
        <div style={{ overflowX:"auto" }}>
          <table>
            <thead><tr><th>Produit</th><th>Total cmds</th><th>Livrées</th><th>Retournées</th><th>Taux livraison</th></tr></thead>
            <tbody>
              {PRODUITS.slice(0,6).map(p => {
                const cmds = commandes.filter(c=>c.produit===p);
                const liv = cmds.filter(c=>c.statut==="Livré").length;
                const ret = cmds.filter(c=>c.statut==="Retourné").length;
                const taux = cmds.length > 0 ? ((liv/cmds.length)*100).toFixed(0) : 0;
                return (
                  <tr key={p}>
                    <td style={{fontWeight:500}}>{p}</td>
                    <td>{cmds.length}</td>
                    <td style={{color:"var(--green)"}}>{liv}</td>
                    <td style={{color:"var(--red)"}}>{ret}</td>
                    <td><div style={{display:"flex",alignItems:"center",gap:"8px"}}>
                      <div style={{flex:1,height:"4px",background:"var(--navy3)",borderRadius:"2px",minWidth:"60px"}}>
                        <div style={{height:"100%",width:`${taux}%`,background:taux>70?"var(--green)":taux>40?"var(--yellow)":"var(--red)",borderRadius:"2px"}}/>
                      </div>
                      <span style={{fontSize:"12px",color:"var(--text)"}}>{taux}%</span>
                    </div></td>
                  </tr>
                );
              })}
            </tbody>
          </table>
        </div>
      </div>
    </div>
  );
}

// ─── COMMANDES ────────────────────────────────────────────────────────────────
function AddOrderModal({ onClose, onAdd }) {
  const [form, setForm] = useState({ client_nom:"", telephone:"", adresse:"", ville:VILLES[0], produit:PRODUITS[0], prix:"", frais_livraison:"30", statut:"Confirmé" });
  const set = (k,v) => setForm(f=>({...f,[k]:v}));
  const submit = (e) => {
    e.preventDefault();
    onAdd({ ...form, id:genId(), agent_id:"u1", agent_nom:"Admin", date_confirmation:new Date().toISOString().split('T')[0], created_at:new Date().toISOString().split('T')[0], prix:Number(form.prix), frais_livraison:Number(form.frais_livraison) });
    onClose();
  };
  return (
    <div className="modal-overlay" onClick={e=>e.target===e.currentTarget&&onClose()}>
      <div className="modal fade-in">
        <div style={{ display:"flex", justifyContent:"space-between", alignItems:"center", marginBottom:"20px" }}>
          <h3 style={{ fontSize:"18px", color:"var(--text)" }}>Nouvelle commande</h3>
          <button className="btn btn-secondary btn-sm" onClick={onClose}><Icon name="close" size={13}/></button>
        </div>
        <form onSubmit={submit}>
          <div className="form-row">
            <div className="form-group"><label>Nom client</label><input value={form.client_nom} onChange={e=>set("client_nom",e.target.value)} style={{width:"100%"}} required/></div>
            <div className="form-group"><label>Téléphone</label><input value={form.telephone} onChange={e=>set("telephone",e.target.value)} style={{width:"100%"}} required/></div>
          </div>
          <div className="form-group"><label>Adresse</label><input value={form.adresse} onChange={e=>set("adresse",e.target.value)} style={{width:"100%"}} required/></div>
          <div className="form-row">
            <div className="form-group"><label>Ville</label><select value={form.ville} onChange={e=>set("ville",e.target.value)} style={{width:"100%"}}>{VILLES.map(v=><option key={v}>{v}</option>)}</select></div>
            <div className="form-group"><label>Statut</label><select value={form.statut} onChange={e=>set("statut",e.target.value)} style={{width:"100%"}}>{STATUTS.map(s=><option key={s}>{s}</option>)}</select></div>
          </div>
          <div className="form-row">
            <div className="form-group"><label>Produit</label><select value={form.produit} onChange={e=>set("produit",e.target.value)} style={{width:"100%"}}>{PRODUITS.map(p=><option key={p}>{p}</option>)}</select></div>
            <div className="form-group"><label>Prix (MAD)</label><input type="number" value={form.prix} onChange={e=>set("prix",e.target.value)} style={{width:"100%"}} required/></div>
          </div>
          <div className="form-group"><label>Frais de livraison (MAD)</label><input type="number" value={form.frais_livraison} onChange={e=>set("frais_livraison",e.target.value)} style={{width:"100%"}} required/></div>
          <div style={{ display:"flex", gap:"10px", justifyContent:"flex-end", marginTop:"8px" }}>
            <button type="button" className="btn btn-secondary" onClick={onClose}>Annuler</button>
            <button type="submit" className="btn btn-primary"><Icon name="check" size={13}/> Enregistrer</button>
          </div>
        </form>
      </div>
    </div>
  );
}

function StatusHistoryModal({ commande, onClose }) {
  const history = [
    { ancien:"—", nouveau:"Confirmé", par:"Admin", at:commande.date_confirmation+" 09:12" },
    { ancien:"Confirmé", nouveau:"En cours", par:"Hamid R.", at:commande.date_confirmation+" 14:30" },
    ...(commande.statut!=="En cours"?[{ ancien:"En cours", nouveau:commande.statut, par:"Admin", at:new Date().toLocaleDateString('fr-CA') }]:[]),
  ];
  return (
    <div className="modal-overlay" onClick={e=>e.target===e.currentTarget&&onClose()}>
      <div className="modal fade-in">
        <div style={{ display:"flex", justifyContent:"space-between", alignItems:"center", marginBottom:"20px" }}>
          <h3 style={{ fontSize:"18px", color:"var(--text)" }}>Historique — #{commande.id}</h3>
          <button className="btn btn-secondary btn-sm" onClick={onClose}><Icon name="close" size={13}/></button>
        </div>
        <div style={{ display:"flex", flexDirection:"column", gap:"10px" }}>
          {history.map((h,i) => (
            <div key={i} style={{ display:"flex", gap:"12px", alignItems:"flex-start" }}>
              <div style={{ width:"8px", height:"8px", borderRadius:"50%", background:"var(--orange)", marginTop:"4px", flexShrink:0 }}/>
              <div>
                <div style={{ fontSize:"13px", color:"var(--text)" }}><span style={{color:"var(--muted)"}}>{h.ancien}</span> → <span style={{color:"var(--orange)"}}>{h.nouveau}</span></div>
                <div style={{ fontSize:"11px", color:"var(--muted)", marginTop:"2px" }}>Par {h.par} · {h.at}</div>
              </div>
            </div>
          ))}
        </div>
      </div>
    </div>
  );
}

function Shipping({ commandes, setCommandes }) {
  const [search, setSearch] = useState("");
  const [filterStatut, setFilterStatut] = useState("");
  const [filterVille, setFilterVille] = useState("");
  const [filterProduit, setFilterProduit] = useState("");
  const [selected, setSelected] = useState([]);
  const [bulkStatut, setBulkStatut] = useState("Livré");
  const [showAdd, setShowAdd] = useState(false);
  const [historyCmd, setHistoryCmd] = useState(null);
  const [importFeedback, setImportFeedback] = useState(null);

  const filtered = useMemo(() => commandes.filter(c => {
    const q = search.toLowerCase();
    return (!q || c.client_nom.toLowerCase().includes(q) || c.id.toLowerCase().includes(q) || c.telephone.includes(q))
      && (!filterStatut || c.statut===filterStatut)
      && (!filterVille || c.ville===filterVille)
      && (!filterProduit || c.produit===filterProduit);
  }), [commandes, search, filterStatut, filterVille, filterProduit]);

  const toggleSelect = (id) => setSelected(s => s.includes(id) ? s.filter(x=>x!==id) : [...s,id]);
  const toggleAll = () => setSelected(selected.length===filtered.length ? [] : filtered.map(c=>c.id));
  const changeStatut = (id, statut) => setCommandes(cs => cs.map(c=>c.id===id?{...c,statut}:c));
  const applyBulk = () => { setCommandes(cs=>cs.map(c=>selected.includes(c.id)?{...c,statut:bulkStatut}:c)); setSelected([]); };
  const addOrder = (cmd) => setCommandes(cs=>[cmd,...cs]);

  const handleImport = (e) => {
    const file = e.target.files[0];
    if(!file) return;
    setImportFeedback({ type:"success", msg:`Import simulé: 12 commandes ajoutées depuis ${file.name}` });
    setTimeout(()=>setImportFeedback(null), 4000);
    e.target.value="";
  };

  return (
    <div className="fade-in">
      <div style={{ display:"flex", alignItems:"center", justifyContent:"space-between", marginBottom:"24px", flexWrap:"wrap", gap:"12px" }}>
        <div>
          <h2 style={{ fontSize:"24px", color:"var(--text)" }}>Gestion des commandes</h2>
          <p style={{ color:"var(--muted)", fontSize:"13px" }}>{commandes.length} commandes au total</p>
        </div>
        <div style={{ display:"flex", gap:"8px", flexWrap:"wrap" }}>
          <label className="btn btn-secondary btn-sm" style={{ cursor:"pointer" }}>
            <Icon name="upload" size={13}/> Import Excel
            <input type="file" accept=".xlsx,.csv" style={{ display:"none" }} onChange={handleImport}/>
          </label>
          <button className="btn btn-secondary btn-sm" onClick={() => alert("Template Excel téléchargé (simulé)")}>
            <Icon name="download" size={13}/> Template
          </button>
          <button className="btn btn-primary btn-sm" onClick={()=>setShowAdd(true)}>
            <Icon name="plus" size={13}/> Nouvelle commande
          </button>
        </div>
      </div>

      {importFeedback && (
        <div style={{ background:"#14532d", border:"1px solid #166534", borderRadius:"6px", padding:"10px 14px", color:"#86efac", fontSize:"13px", marginBottom:"16px", display:"flex", justifyContent:"space-between" }}>
          {importFeedback.msg}
          <span style={{cursor:"pointer"}} onClick={()=>setImportFeedback(null)}>×</span>
        </div>
      )}

      {/* Filters */}
      <div style={{ display:"flex", gap:"8px", flexWrap:"wrap", marginBottom:"16px" }}>
        <div style={{ position:"relative", flex:1, minWidth:"180px" }}>
          <span style={{ position:"absolute", left:"10px", top:"50%", transform:"translateY(-50%)", color:"var(--muted)" }}><Icon name="search" size={13}/></span>
          <input placeholder="Rechercher client, ID, téléphone..." value={search} onChange={e=>setSearch(e.target.value)} style={{ width:"100%", paddingLeft:"32px" }}/>
        </div>
        <select value={filterStatut} onChange={e=>setFilterStatut(e.target.value)}>
          <option value="">Tous les statuts</option>
          {STATUTS.map(s=><option key={s}>{s}</option>)}
        </select>
        <select value={filterVille} onChange={e=>setFilterVille(e.target.value)}>
          <option value="">Toutes les villes</option>
          {VILLES.map(v=><option key={v}>{v}</option>)}
        </select>
        <select value={filterProduit} onChange={e=>setFilterProduit(e.target.value)}>
          <option value="">Tous les produits</option>
          {PRODUITS.map(p=><option key={p}>{p}</option>)}
        </select>
      </div>

      {/* Bulk actions */}
      {selected.length > 0 && (
        <div style={{ background:"var(--navy3)", border:"1px solid var(--orange)", borderRadius:"8px", padding:"10px 14px", marginBottom:"14px", display:"flex", alignItems:"center", gap:"12px", flexWrap:"wrap" }}>
          <span style={{ color:"var(--orange)", fontSize:"13px", fontWeight:500 }}>{selected.length} commande(s) sélectionnée(s)</span>
          <select value={bulkStatut} onChange={e=>setBulkStatut(e.target.value)}>
            {STATUTS.map(s=><option key={s}>{s}</option>)}
          </select>
          <button className="btn btn-primary btn-sm" onClick={applyBulk}><Icon name="check" size={12}/> Appliquer</button>
          <button className="btn btn-secondary btn-sm" onClick={()=>setSelected([])}>Annuler</button>
        </div>
      )}

      {/* Table */}
      <div className="card" style={{ padding:0, overflow:"hidden" }}>
        <div style={{ overflowX:"auto" }}>
          <table>
            <thead>
              <tr>
                <th><input type="checkbox" className="checkbox-custom" checked={selected.length===filtered.length&&filtered.length>0} onChange={toggleAll}/></th>
                <th>ID</th><th>Client</th><th>Téléphone</th><th>Ville</th><th>Produit</th><th>Prix</th><th>Frais</th><th>Statut</th><th>Date</th><th>Agent</th><th>Actions</th>
              </tr>
            </thead>
            <tbody>
              {filtered.length===0 && (
                <tr><td colSpan={12} style={{ textAlign:"center", color:"var(--muted)", padding:"40px" }}>Aucune commande trouvée</td></tr>
              )}
              {filtered.map(c => (
                <tr key={c.id}>
                  <td><input type="checkbox" className="checkbox-custom" checked={selected.includes(c.id)} onChange={()=>toggleSelect(c.id)}/></td>
                  <td style={{ fontFamily:"monospace", fontSize:"12px", color:"var(--orange)" }}>{c.id}</td>
                  <td style={{ fontWeight:500 }}>{c.client_nom}</td>
                  <td style={{ color:"var(--muted)" }}>{c.telephone}</td>
                  <td>{c.ville}</td>
                  <td style={{ maxWidth:"120px", overflow:"hidden", textOverflow:"ellipsis", whiteSpace:"nowrap" }}>{c.produit}</td>
                  <td style={{ fontWeight:500 }}>{fmtMAD(c.prix)}</td>
                  <td style={{ color:"var(--muted)" }}>{c.frais_livraison} MAD</td>
                  <td>
                    <select value={c.statut} onChange={e=>changeStatut(c.id,e.target.value)} style={{ padding:"4px 8px", fontSize:"11px", border:"none", background:"transparent" }}
                      className={badgeClass(c.statut).replace("badge ","")}>
                      {STATUTS.map(s=><option key={s}>{s}</option>)}
                    </select>
                  </td>
                  <td style={{ color:"var(--muted)", fontSize:"12px" }}>{c.date_confirmation}</td>
                  <td style={{ fontSize:"12px" }}>{c.agent_nom}</td>
                  <td>
                    <div style={{ display:"flex", gap:"4px" }}>
                      <button className="btn btn-secondary btn-sm" title="Historique" onClick={()=>setHistoryCmd(c)}><Icon name="history" size={12}/></button>
                    </div>
                  </td>
                </tr>
              ))}
            </tbody>
          </table>
        </div>
      </div>

      {showAdd && <AddOrderModal onClose={()=>setShowAdd(false)} onAdd={addOrder}/>}
      {historyCmd && <StatusHistoryModal commande={historyCmd} onClose={()=>setHistoryCmd(null)}/>}
    </div>
  );
}

// ─── ÉTIQUETTES ───────────────────────────────────────────────────────────────
function ShippingMark({ commandes }) {
  const [selected, setSelected] = useState([]);
  const [search, setSearch] = useState("");
  const [preview, setPreview] = useState(null);

  const filtered = commandes.filter(c => {
    const q = search.toLowerCase();
    return !q || c.client_nom.toLowerCase().includes(q) || c.id.toLowerCase().includes(q);
  });

  const toggleSelect = (id) => setSelected(s=>s.includes(id)?s.filter(x=>x!==id):[...s,id]);
  const toggleAll = () => setSelected(selected.length===filtered.length?[]:filtered.map(c=>c.id));

  const printSelected = () => {
    const cmds = commandes.filter(c=>selected.includes(c.id));
    if(cmds.length===0) return;
    setPreview(cmds);
  };

  const LabelCard = ({ cmd, forPrint }) => (
    <div style={{ border:"2px solid #333", borderRadius:forPrint?"0":"8px", padding:"16px", background:"white", color:"#111", fontFamily:"sans-serif", width:forPrint?"100%":"280px", flexShrink:0, pageBreakAfter:"always" }}>
      <div style={{ display:"flex", justifyContent:"space-between", alignItems:"flex-start", marginBottom:"12px", borderBottom:"2px solid #f5820a", paddingBottom:"10px" }}>
        <div>
          <div style={{ fontSize:"14px", fontWeight:800, letterSpacing:"0.05em", color:"#f5820a" }}>IMAKLOGISTIC</div>
          <div style={{ fontSize:"10px", color:"#666" }}>Bon de livraison</div>
        </div>
        <div style={{ textAlign:"right" }}>
          <div style={{ fontSize:"10px", color:"#666" }}>ID Commande</div>
          <div style={{ fontSize:"13px", fontWeight:700, fontFamily:"monospace", color:"#f5820a" }}>#{cmd.id}</div>
        </div>
      </div>
      <div style={{ marginBottom:"8px" }}>
        <div style={{ fontSize:"10px", textTransform:"uppercase", color:"#888", marginBottom:"2px" }}>Destinataire</div>
        <div style={{ fontSize:"14px", fontWeight:700 }}>{cmd.client_nom}</div>
        <div style={{ fontSize:"12px", color:"#444" }}>{cmd.telephone}</div>
      </div>
      <div style={{ background:"#f5f5f5", borderRadius:"4px", padding:"8px", marginBottom:"8px" }}>
        <div style={{ fontSize:"10px", textTransform:"uppercase", color:"#888", marginBottom:"2px" }}>Adresse de livraison</div>
        <div style={{ fontSize:"12px", fontWeight:500 }}>{cmd.adresse}</div>
        <div style={{ fontSize:"12px", fontWeight:700, color:"#f5820a" }}>{cmd.ville}</div>
      </div>
      <div style={{ marginBottom:"8px" }}>
        <div style={{ fontSize:"10px", textTransform:"uppercase", color:"#888", marginBottom:"2px" }}>Produit</div>
        <div style={{ fontSize:"12px", fontWeight:600 }}>{cmd.produit}</div>
      </div>
      <div style={{ display:"flex", justifyContent:"space-between", background:"#1a1a2e", color:"white", borderRadius:"4px", padding:"8px 10px" }}>
        <div style={{ fontSize:"10px" }}>Prix: <span style={{ fontWeight:700, fontSize:"13px" }}>{cmd.prix} MAD</span></div>
        <div style={{ fontSize:"10px" }}>Frais: <span style={{ fontWeight:700, fontSize:"13px" }}>{cmd.frais_livraison} MAD</span></div>
        <div style={{ fontSize:"10px" }}>Total: <span style={{ fontWeight:700, fontSize:"13px", color:"#f5820a" }}>{cmd.prix+cmd.frais_livraison} MAD</span></div>
      </div>
      <div style={{ textAlign:"center", marginTop:"10px", fontSize:"9px", color:"#aaa" }}>
        {/* QR code placeholder */}
        <div style={{ width:"50px", height:"50px", background:"#eee", margin:"0 auto 4px", display:"flex", alignItems:"center", justifyContent:"center", borderRadius:"4px", fontSize:"8px", color:"#999", fontWeight:600 }}>QR</div>
        Date: {cmd.date_confirmation}
      </div>
    </div>
  );

  return (
    <div className="fade-in">
      <div style={{ display:"flex", alignItems:"center", justifyContent:"space-between", marginBottom:"24px", flexWrap:"wrap", gap:"12px" }}>
        <div>
          <h2 style={{ fontSize:"24px", color:"var(--text)" }}>Étiquettes d'expédition</h2>
          <p style={{ color:"var(--muted)", fontSize:"13px" }}>Générer et imprimer les bons de livraison</p>
        </div>
        <div style={{ display:"flex", gap:"8px" }}>
          {selected.length>0 && (
            <button className="btn btn-primary" onClick={printSelected}><Icon name="print" size={14}/> Imprimer ({selected.length})</button>
          )}
        </div>
      </div>

      <div style={{ marginBottom:"14px" }}>
        <div style={{ position:"relative", maxWidth:"320px" }}>
          <span style={{ position:"absolute", left:"10px", top:"50%", transform:"translateY(-50%)", color:"var(--muted)" }}><Icon name="search" size={13}/></span>
          <input placeholder="Rechercher..." value={search} onChange={e=>setSearch(e.target.value)} style={{ width:"100%", paddingLeft:"32px" }}/>
        </div>
      </div>

      {selected.length>0 && <div style={{ marginBottom:"12px", padding:"8px 14px", background:"rgba(245,130,10,0.08)", border:"1px solid rgba(245,130,10,0.25)", borderRadius:"6px", fontSize:"13px", color:"var(--orange)" }}>{selected.length} étiquette(s) sélectionnée(s)</div>}

      <div className="card" style={{ padding:0, overflow:"hidden" }}>
        <div style={{ overflowX:"auto" }}>
          <table>
            <thead><tr>
              <th><input type="checkbox" className="checkbox-custom" checked={selected.length===filtered.length&&filtered.length>0} onChange={toggleAll}/></th>
              <th>ID</th><th>Client</th><th>Téléphone</th><th>Adresse</th><th>Ville</th><th>Produit</th><th>Statut</th><th>Aperçu</th>
            </tr></thead>
            <tbody>
              {filtered.map(c=>(
                <tr key={c.id}>
                  <td><input type="checkbox" className="checkbox-custom" checked={selected.includes(c.id)} onChange={()=>toggleSelect(c.id)}/></td>
                  <td style={{ fontFamily:"monospace",fontSize:"12px",color:"var(--orange)" }}>{c.id}</td>
                  <td style={{ fontWeight:500 }}>{c.client_nom}</td>
                  <td style={{ color:"var(--muted)" }}>{c.telephone}</td>
                  <td style={{ color:"var(--muted)",fontSize:"12px" }}>{c.adresse}</td>
                  <td>{c.ville}</td>
                  <td>{c.produit}</td>
                  <td><span className={badgeClass(c.statut)}>{c.statut}</span></td>
                  <td><button className="btn btn-secondary btn-sm" onClick={()=>setPreview([c])}><Icon name="eye" size={12}/></button></td>
                </tr>
              ))}
            </tbody>
          </table>
        </div>
      </div>

      {/* Preview Modal */}
      {preview && (
        <div className="modal-overlay" onClick={e=>e.target===e.currentTarget&&setPreview(null)}>
          <div style={{ background:"var(--navy2)", border:"1px solid var(--border)", borderRadius:"12px", padding:"24px", width:"100%", maxWidth:"860px", maxHeight:"90vh", overflow:"auto" }} className="fade-in">
            <div style={{ display:"flex", justifyContent:"space-between", alignItems:"center", marginBottom:"20px" }} className="no-print">
              <h3 style={{ fontSize:"18px", color:"var(--text)" }}>Aperçu — {preview.length} étiquette(s)</h3>
              <div style={{ display:"flex", gap:"8px" }}>
                <button className="btn btn-primary btn-sm" onClick={()=>window.print()}><Icon name="print" size={13}/> Imprimer</button>
                <button className="btn btn-secondary btn-sm" onClick={()=>setPreview(null)}><Icon name="close" size={13}/></button>
              </div>
            </div>
            <div style={{ display:"flex", flexWrap:"wrap", gap:"16px" }}>
              {preview.map(c=><LabelCard key={c.id} cmd={c}/>)}
            </div>
          </div>
        </div>
      )}
    </div>
  );
}

// ─── FACTURATION ──────────────────────────────────────────────────────────────
function Facturation({ commandes, user }) {
  const [factures, setFactures] = useState(() => {
    const week = getWeekRange();
    const lignes = commandes.filter(c=>c.statut==="Livré"||c.statut==="Remboursé");
    return [{
      id: "FAC-2025-001",
      semaine_debut: week.start, semaine_fin: week.end,
      statut: "ouverte",
      lignes: lignes.map(c=>({ commande_id:c.id, client:c.client_nom, produit:c.produit, prix:c.prix, frais_livraison:c.frais_livraison, type:c.statut==="Remboursé"?"remboursement":"livraison" })),
    }];
  });

  const [selected, setSelected] = useState(0);
  const facture = factures[selected];

  const totals = useMemo(() => {
    if(!facture) return {};
    const livraisons = facture.lignes.filter(l=>l.type==="livraison");
    const remboursements = facture.lignes.filter(l=>l.type==="remboursement");
    const subtotal = livraisons.reduce((s,l)=>s+l.prix,0);
    const totalFrais = livraisons.reduce((s,l)=>s+l.frais_livraison,0);
    const deductions = remboursements.reduce((s,l)=>s+l.prix,0);
    const net = subtotal - deductions + totalFrais;
    return { subtotal, totalFrais, deductions, net, livraisons:livraisons.length, remboursements:remboursements.length };
  }, [facture]);

  const cloturerFacture = () => {
    if(!window.confirm("Clôturer cette facture ? Cette action est irréversible.")) return;
    setFactures(fs => fs.map((f,i) => i===selected ? {...f, statut:"clôturée", cloturée_par:user.name, cloturée_at:new Date().toISOString()} : f));
    const week = getWeekRange(new Date(Date.now()+7*86400000));
    setFactures(fs => [...fs, { id:`FAC-2025-${String(fs.length+1).padStart(3,"0")}`, semaine_debut:week.start, semaine_fin:week.end, statut:"ouverte", lignes:[] }]);
    setSelected(factures.length);
  };

  const updateFrais = (idx, val) => {
    setFactures(fs => fs.map((f,i) => i===selected ? {...f, lignes:f.lignes.map((l,j)=>j===idx?{...l,frais_livraison:Number(val)}:l)} : f));
  };

  if(!facture) return null;

  return (
    <div className="fade-in">
      <div style={{ display:"flex", alignItems:"center", justifyContent:"space-between", marginBottom:"24px", flexWrap:"wrap", gap:"12px" }}>
        <div>
          <h2 style={{ fontSize:"24px", color:"var(--text)" }}>Facturation</h2>
          <p style={{ color:"var(--muted)", fontSize:"13px" }}>Gestion des factures hebdomadaires</p>
        </div>
        <div style={{ display:"flex", gap:"8px" }}>
          {facture.statut==="ouverte" && (
            <button className="btn btn-danger" onClick={cloturerFacture}><Icon name="lock" size={14}/> Clôturer la facture</button>
          )}
          <button className="btn btn-primary" onClick={()=>alert("Téléchargement PDF simulé")}><Icon name="download" size={14}/> Télécharger PDF</button>
        </div>
      </div>

      {/* Facture selector */}
      <div style={{ display:"flex", gap:"8px", marginBottom:"20px", flexWrap:"wrap" }}>
        {factures.map((f,i) => (
          <div key={f.id} className={`tab${selected===i?" active":""}`} onClick={()=>setSelected(i)} style={{ display:"flex", alignItems:"center", gap:"8px" }}>
            {f.id}
            <span style={{ padding:"2px 6px", borderRadius:"3px", fontSize:"10px", background:f.statut==="ouverte"?"rgba(34,197,94,0.15)":"rgba(120,120,120,0.15)", color:f.statut==="ouverte"?"var(--green)":"var(--muted)" }}>
              {f.statut}
            </span>
          </div>
        ))}
      </div>

      {/* Invoice header */}
      <div className="card" style={{ marginBottom:"14px", background:"linear-gradient(135deg,var(--navy3),var(--navy2))" }}>
        <div style={{ display:"flex", justifyContent:"space-between", alignItems:"flex-start", flexWrap:"wrap", gap:"16px" }}>
          <div>
            <div style={{ display:"flex", alignItems:"center", gap:"10px", marginBottom:"8px" }}>
              <div style={{ width:"32px", height:"32px", background:"var(--orange)", borderRadius:"6px", display:"flex", alignItems:"center", justifyContent:"center" }}>
                <Icon name="invoice" size={16}/>
              </div>
              <h3 style={{ fontSize:"20px", color:"var(--text)" }}>{facture.id}</h3>
            </div>
            <div style={{ fontSize:"13px", color:"var(--muted)" }}>Période: <span style={{ color:"var(--text)" }}>{facture.semaine_debut}</span> → <span style={{ color:"var(--text)" }}>{facture.semaine_fin}</span></div>
            {facture.cloturée_par && <div style={{ fontSize:"12px", color:"var(--muted)", marginTop:"4px" }}>Clôturée par {facture.cloturée_par}</div>}
          </div>
          <div style={{ display:"grid", gridTemplateColumns:"1fr 1fr", gap:"12px" }}>
            {[
              { l:"Commandes livrées", v:totals.livraisons, c:"var(--green)" },
              { l:"Remboursements", v:totals.remboursements, c:"var(--red)" },
              { l:"Sous-total", v:fmtMAD(totals.subtotal), c:"var(--text)" },
              { l:"TOTAL NET", v:fmtMAD(totals.net), c:"var(--orange)" },
            ].map(item=>(
              <div key={item.l} style={{ textAlign:"right" }}>
                <div style={{ fontSize:"11px", color:"var(--muted)", marginBottom:"2px" }}>{item.l}</div>
                <div style={{ fontSize:"16px", fontFamily:"'Barlow Condensed',sans-serif", fontWeight:700, color:item.c }}>{item.v}</div>
              </div>
            ))}
          </div>
        </div>
      </div>

      {/* Lines table */}
      <div className="card" style={{ padding:0, overflow:"hidden" }}>
        <div style={{ padding:"16px 20px", borderBottom:"1px solid var(--border)", display:"flex", justifyContent:"space-between", alignItems:"center" }}>
          <h4 style={{ fontSize:"14px", color:"var(--text)" }}>Lignes de facturation ({facture.lignes.length})</h4>
          {facture.statut==="ouverte" && <span style={{ fontSize:"12px", color:"var(--muted)" }}>Modifiez les frais directement dans le tableau</span>}
        </div>
        <div style={{ overflowX:"auto" }}>
          <table>
            <thead><tr><th>#</th><th>Client</th><th>Produit</th><th>Prix</th><th>Frais livraison</th><th>Type</th></tr></thead>
            <tbody>
              {facture.lignes.length===0 && <tr><td colSpan={6} style={{ textAlign:"center", color:"var(--muted)", padding:"40px" }}>Aucune ligne pour cette période</td></tr>}
              {facture.lignes.map((l,i)=>(
                <tr key={i}>
                  <td style={{ color:"var(--muted)", fontSize:"12px" }}>{i+1}</td>
                  <td style={{ fontWeight:500 }}>{l.client}</td>
                  <td>{l.produit}</td>
                  <td style={{ fontFamily:"monospace" }}>{l.prix} MAD</td>
                  <td>
                    {facture.statut==="ouverte" ? (
                      <input type="number" value={l.frais_livraison} onChange={e=>updateFrais(i,e.target.value)} style={{ width:"90px", padding:"4px 8px" }}/>
                    ) : (
                      <span style={{ fontFamily:"monospace" }}>{l.frais_livraison} MAD</span>
                    )}
                  </td>
                  <td><span className={l.type==="livraison"?"badge badge-livré":"badge badge-remboursé"}>{l.type}</span></td>
                </tr>
              ))}
            </tbody>
            {facture.lignes.length>0 && (
              <tfoot>
                <tr style={{ background:"var(--navy3)" }}>
                  <td colSpan={3} style={{ color:"var(--muted)", fontSize:"12px", textAlign:"right", fontWeight:600 }}>TOTAL</td>
                  <td style={{ fontWeight:700, color:"var(--text)", fontFamily:"monospace" }}>{totals.subtotal} MAD</td>
                  <td style={{ fontWeight:700, color:"var(--text)", fontFamily:"monospace" }}>{totals.totalFrais} MAD</td>
                  <td></td>
                </tr>
                <tr style={{ background:"rgba(245,130,10,0.05)" }}>
                  <td colSpan={5} style={{ textAlign:"right", fontSize:"11px", color:"var(--muted)", paddingTop:"8px" }}>
                    Sous-total livraisons: {totals.subtotal} MAD — Déductions: -{totals.deductions} MAD — Frais: +{totals.totalFrais} MAD
                  </td>
                  <td></td>
                </tr>
                <tr style={{ background:"rgba(245,130,10,0.08)" }}>
                  <td colSpan={4} style={{ textAlign:"right", fontFamily:"'Barlow Condensed',sans-serif", fontSize:"18px", color:"var(--orange)", fontWeight:700 }}>TOTAL NET</td>
                  <td colSpan={2} style={{ fontFamily:"'Barlow Condensed',sans-serif", fontSize:"22px", color:"var(--orange)", fontWeight:700 }}>{fmtMAD(totals.net)}</td>
                </tr>
              </tfoot>
            )}
          </table>
        </div>
      </div>
    </div>
  );
}

// ─── ACCESS MANAGEMENT ────────────────────────────────────────────────────────
const ALL_MODULES = [
  { id:"dashboard", label:"Tableau de bord" },
  { id:"shipping", label:"Commandes" },
  { id:"shipping_mark", label:"Étiquettes" },
  { id:"facturation", label:"Facturation" },
  { id:"access", label:"Accès & Utilisateurs" },
];

function UserModal({ user:initial, onClose, onSave }) {
  const [form, setForm] = useState(initial || { name:"", email:"", password:"", role:"agent", permissions:["dashboard","shipping"] });
  const set = (k,v) => setForm(f=>({...f,[k]:v}));
  const togglePerm = (p) => set("permissions", form.permissions.includes(p) ? form.permissions.filter(x=>x!==p) : [...form.permissions,p]);
  const submit = (e) => { e.preventDefault(); onSave({...form, id:initial?.id||genId()}); onClose(); };

  return (
    <div className="modal-overlay" onClick={e=>e.target===e.currentTarget&&onClose()}>
      <div className="modal fade-in">
        <div style={{ display:"flex", justifyContent:"space-between", alignItems:"center", marginBottom:"20px" }}>
          <h3 style={{ fontSize:"18px", color:"var(--text)" }}>{initial?"Modifier":"Nouvel"} utilisateur</h3>
          <button className="btn btn-secondary btn-sm" onClick={onClose}><Icon name="close" size={13}/></button>
        </div>
        <form onSubmit={submit}>
          <div className="form-row">
            <div className="form-group"><label>Nom complet</label><input value={form.name} onChange={e=>set("name",e.target.value)} style={{width:"100%"}} required/></div>
            <div className="form-group"><label>Email</label><input type="email" value={form.email} onChange={e=>set("email",e.target.value)} style={{width:"100%"}} required/></div>
          </div>
          <div className="form-row">
            <div className="form-group"><label>Mot de passe{initial?" (laisser vide pour ne pas changer)":""}</label><input type="password" value={form.password} onChange={e=>set("password",e.target.value)} style={{width:"100%"}} {...(!initial?{required:true}:{})}/></div>
            <div className="form-group"><label>Rôle</label>
              <select value={form.role} onChange={e=>set("role",e.target.value)} style={{width:"100%"}}>
                <option value="super_admin">Super Admin</option>
                <option value="admin">Admin</option>
                <option value="agent">Agent</option>
              </select>
            </div>
          </div>
          <div className="form-group">
            <label>Modules accessibles</label>
            <div style={{ display:"flex", flexDirection:"column", gap:"8px", marginTop:"4px" }}>
              {ALL_MODULES.map(m=>(
                <label key={m.id} style={{ display:"flex", alignItems:"center", gap:"10px", cursor:"pointer", fontSize:"13px", color:"var(--text)" }}>
                  <input type="checkbox" className="checkbox-custom" checked={form.permissions.includes(m.id)} onChange={()=>togglePerm(m.id)}/>
                  {m.label}
                </label>
              ))}
            </div>
          </div>
          <div style={{ display:"flex", gap:"10px", justifyContent:"flex-end", marginTop:"8px" }}>
            <button type="button" className="btn btn-secondary" onClick={onClose}>Annuler</button>
            <button type="submit" className="btn btn-primary"><Icon name="check" size={13}/> Enregistrer</button>
          </div>
        </form>
      </div>
    </div>
  );
}

function AccessManagement() {
  const [users, setUsers] = useState(MOCK_USERS);
  const [modal, setModal] = useState(null); // null | "add" | user object

  const saveUser = (u) => {
    setUsers(us => us.find(x=>x.id===u.id) ? us.map(x=>x.id===u.id?u:x) : [...us,u]);
  };
  const deleteUser = (id) => { if(window.confirm("Supprimer cet utilisateur ?")) setUsers(us=>us.filter(u=>u.id!==id)); };
  const roleColor = { super_admin:"var(--orange)", admin:"var(--blue)", agent:"var(--green)" };

  return (
    <div className="fade-in">
      <div style={{ display:"flex", alignItems:"center", justifyContent:"space-between", marginBottom:"24px" }}>
        <div>
          <h2 style={{ fontSize:"24px", color:"var(--text)" }}>Accès & Utilisateurs</h2>
          <p style={{ color:"var(--muted)", fontSize:"13px" }}>{users.length} compte(s) actif(s)</p>
        </div>
        <button className="btn btn-primary" onClick={()=>setModal("add")}><Icon name="plus" size={14}/> Nouvel utilisateur</button>
      </div>

      <div style={{ display:"flex", flexDirection:"column", gap:"12px" }}>
        {users.map(u=>(
          <div key={u.id} className="card" style={{ display:"flex", alignItems:"center", justifyContent:"space-between", flexWrap:"wrap", gap:"14px" }}>
            <div style={{ display:"flex", alignItems:"center", gap:"14px" }}>
              <div style={{ width:"42px", height:"42px", borderRadius:"50%", background:"var(--navy3)", border:"2px solid var(--border)", display:"flex", alignItems:"center", justifyContent:"center", fontSize:"16px", fontWeight:700, color:roleColor[u.role]||"var(--text)" }}>
                {u.name.charAt(0)}
              </div>
              <div>
                <div style={{ fontSize:"15px", color:"var(--text)", fontWeight:500 }}>{u.name}</div>
                <div style={{ fontSize:"12px", color:"var(--muted)" }}>{u.email}</div>
              </div>
              <span style={{ padding:"3px 8px", borderRadius:"4px", fontSize:"11px", fontWeight:600, textTransform:"uppercase", letterSpacing:"0.04em", background:u.role==="super_admin"?"rgba(245,130,10,0.12)":u.role==="admin"?"rgba(59,130,246,0.12)":"rgba(34,197,94,0.12)", color:roleColor[u.role]||"var(--muted)" }}>
                {u.role.replace("_"," ")}
              </span>
            </div>
            <div style={{ display:"flex", gap:"6px", flexWrap:"wrap", flex:1, justifyContent:"center" }}>
              {ALL_MODULES.map(m=>(
                <span key={m.id} style={{ padding:"3px 8px", borderRadius:"4px", fontSize:"11px", background:u.permissions.includes(m.id)?"rgba(34,197,94,0.1)":"var(--navy3)", color:u.permissions.includes(m.id)?"var(--green)":"var(--muted)", border:"1px solid", borderColor:u.permissions.includes(m.id)?"rgba(34,197,94,0.2)":"var(--border)" }}>
                  {u.permissions.includes(m.id)?"✓":""} {m.label}
                </span>
              ))}
            </div>
            <div style={{ display:"flex", gap:"6px" }}>
              <button className="btn btn-secondary btn-sm" onClick={()=>setModal(u)}><Icon name="edit" size={12}/></button>
              <button className="btn btn-danger btn-sm" onClick={()=>deleteUser(u.id)}><Icon name="trash" size={12}/></button>
            </div>
          </div>
        ))}
      </div>

      {modal && (
        <UserModal user={modal==="add"?null:modal} onClose={()=>setModal(null)} onSave={saveUser}/>
      )}
    </div>
  );
}

// ─── MAIN APP ─────────────────────────────────────────────────────────────────
export default function App() {
  const [user, setUser] = useState(null);
  const [active, setActive] = useState("dashboard");
  const [commandes, setCommandes] = useState(MOCK_COMMANDES);

  const handleLogin = (u) => { setUser(u); setActive(u.permissions[0]||"dashboard"); };
  const handleLogout = () => setUser(null);

  if(!user) return <LoginPage onLogin={handleLogin}/>;

  const renderModule = () => {
    switch(active) {
      case "dashboard": return <Dashboard commandes={commandes}/>;
      case "shipping": return <Shipping commandes={commandes} setCommandes={setCommandes}/>;
      case "shipping_mark": return <ShippingMark commandes={commandes}/>;
      case "facturation": return <Facturation commandes={commandes} user={user}/>;
      case "access": return <AccessManagement/>;
      default: return <div style={{color:"var(--muted)"}}>Module non disponible</div>;
    }
  };

  return (
    <div style={{ display:"flex", minHeight:"100vh", background:"var(--navy)" }}>
      <Sidebar user={user} active={active} setActive={setActive} onLogout={handleLogout}/>
      <main style={{ flex:1, marginLeft:"220px", padding:"28px", maxWidth:"calc(100vw - 220px)", minHeight:"100vh" }}>
        {renderModule()}
      </main>
    </div>
  );
}
