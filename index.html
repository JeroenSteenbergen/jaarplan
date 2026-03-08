import { useState } from "react";

const FRIENDS = ["Tom", "Daan", "Rinze", "Folkert", "Vincent", "Jeroen", "Wynfrith"];

const CATEGORIES = [
  { id: "hobby",        label: "Nieuwe Hobby",                 emoji: "🎨" },
  { id: "kennis",       label: "Verdiepen Nieuw Onderwerp",    emoji: "📚" },
  { id: "sport",        label: "Grensverleggend Sportief",     emoji: "⚡" },
  { id: "maatschappij", label: "Maatschappelijke Bijdrage",    emoji: "🌱" },
  { id: "vrienden",     label: "Iets Speciaals met Vrienden",  emoji: "🤝" },
];

const INITIAL_DATA = [];

const G = "#1A7A4A";
const GL = "#E8F5EE";
const GB = "#B8DEC9";

const INSPIRATIE = {
  hobby: [
    "Aquarelverf — eerste schilderij maken en ophangen",
    "Broodbakken — zuurdesembrood van scratch leren maken",
    "Schaken — de basisopeningen leren en een toernooi spelen",
    "Fotografie — een dag op pad met alleen een analoge camera",
    "Timmeren — een meubel bouwen zonder kant-en-klare instructies",
  ],
  kennis: [
    "Astronomie — sterrenkijker aanschaffen en 10 objecten identificeren",
    "Filosofie — drie klassieke werken lezen en erover discussiëren",
    "Economie — een boek over gedragseconomie lezen én toepassen",
    "Geschiedenis — een documentairereeks volgen over een onbekend tijdperk",
    "Psychologie — een cursus cognitieve gedragstherapie volgen",
  ],
  sport: [
    "Koud water zwemmen — drie keer in open water zwemmen in de winter",
    "Klimmen — een indoor bouldergraad halen die je nog nooit haalde",
    "Fietsen — een tocht van 100+ km in één dag voltooien",
    "Triathlon — deelnemen aan een sprint triathlon",
    "Vechtsport — een bokstraining of judoles bijwonen en voltooien",
  ],
  maatschappij: [
    "Bloeddonatie — drie keer bloed doneren in één jaar",
    "Mentorschap — een scholier of student een semester begeleiden",
    "Repair café — spullen van anderen gratis repareren",
    "Schoonmaakactie — eigen buurt of park opruimen met een groepje",
    "Voedselbos — meehelpen aanplanten of onderhouden van een stadsnatuurproject",
  ],
  vrienden: [
    "Weekendwandeling — meerdaagse trekking door Nederland of Duitsland",
    "Koken voor de groep — volledig 3-gangenmenu van een vreemde keuken bereiden",
    "Sportdag — zelf een olympiade organiseren met gekke disciplines",
    "Samen leren — met zijn allen een nieuwe vaardigheid oppakken in één dag",
    "Verrassingsdag — iemand verrassen met een volledig georganiseerde dag",
  ],
};

export default function App() {
  const [achievements, setAchievements] = useState(INITIAL_DATA);
  const [showModal, setShowModal] = useState(false);
  const [voter, setVoter] = useState(null);
  const [form, setForm] = useState({ name: "", category: "hobby", description: "" });
  const [notification, setNotification] = useState(null);
  const [animId, setAnimId] = useState(null);
  const [inspOpen, setInspOpen] = useState(null); // catId or null

  const notify = (msg, type = "ok") => {
    setNotification({ msg, type });
    setTimeout(() => setNotification(null), 2500);
  };

  const add = () => {
    if (!form.name || !form.description.trim()) return;
    setAchievements(p => [{ id: Date.now(), ...form, description: form.description.trim(), thumbsUp: [], thumbsDown: [] }, ...p]);
    setShowModal(false);
    setForm({ name: "", category: "hobby", description: "" });
    notify("Prestatie toegevoegd!");
  };

  const vote = (id, type) => {
    if (!voter) { notify("Kies eerst wie je bent!", "err"); return; }
    const item = achievements.find(a => a.id === id);
    if (item.name === voter) { notify("Je kunt niet op jezelf stemmen.", "err"); return; }
    const alreadyUp = item.thumbsUp.includes(voter);
    const alreadyDown = item.thumbsDown.includes(voter);
    setAnimId(id + type);
    setTimeout(() => setAnimId(null), 350);
    setAchievements(p => p.map(a => a.id !== id ? a : ({
      ...a,
      thumbsUp: type === "up"
        ? (alreadyUp ? a.thumbsUp.filter(v => v !== voter) : [...a.thumbsUp.filter(v => v !== voter), voter])
        : a.thumbsUp.filter(v => v !== voter),
      thumbsDown: type === "down"
        ? (alreadyDown ? a.thumbsDown.filter(v => v !== voter) : [...a.thumbsDown.filter(v => v !== voter), voter])
        : a.thumbsDown.filter(v => v !== voter),
    })));
    if (type === "up") notify(alreadyUp ? "Duim omhoog ingetrokken." : "Duim omhoog!");
    else notify(alreadyDown ? "Duim omlaag ingetrokken." : "Duim omlaag.");
  };

  const deleteAchievement = (id) => {
    setAchievements(p => p.filter(a => a.id !== id));
    notify("Prestatie verwijderd.");
  };

  const sorted = (catId) =>
    achievements.filter(a => a.category === catId)
      .sort((a, b) => (b.thumbsUp.length - b.thumbsDown.length) - (a.thumbsUp.length - a.thumbsDown.length));

  return (
    <div style={{ minHeight: "100vh", background: "#F2F5F3", fontFamily: "'Segoe UI', Arial, sans-serif", color: "#1C2B22" }}>

      {notification && (
        <div style={{
          position: "fixed", top: 16, left: "50%", transform: "translateX(-50%)",
          background: notification.type === "err" ? "#B91C1C" : G,
          color: "#fff", padding: "9px 22px", borderRadius: 3,
          fontWeight: 600, fontSize: 13, zIndex: 9999, boxShadow: "0 4px 14px rgba(0,0,0,0.2)",
          animation: "sd 0.22s ease", whiteSpace: "nowrap",
        }}>{notification.msg}</div>
      )}

      {/* Header */}
      <div style={{ background: G, padding: "14px 24px", display: "flex", justifyContent: "space-between", alignItems: "center", flexWrap: "wrap", gap: 12 }}>
        <div>
          <div style={{ fontSize: 10, letterSpacing: 3, color: "rgba(255,255,255,0.55)", textTransform: "uppercase", fontWeight: 700 }}>De Vriendenkring</div>
          <h1 style={{ margin: "2px 0 0", fontSize: 20, fontWeight: 800, color: "#fff" }}>Jaarplan 2026</h1>
          <div style={{ fontSize: 11, color: "rgba(255,255,255,0.5)", marginTop: 2 }}>{FRIENDS.join(" · ")}</div>
        </div>
        <div style={{ display: "flex", gap: 10, alignItems: "center", flexWrap: "wrap" }}>
          <select value={voter || ""} onChange={e => setVoter(e.target.value || null)}
            style={{ background: "#fff", border: "none", borderRadius: 3, padding: "8px 14px", fontSize: 13, color: voter ? G : "#888", fontWeight: voter ? 700 : 400, cursor: "pointer", outline: "none" }}>
            <option value="">Wie ben jij?</option>
            {FRIENDS.map(f => <option key={f} value={f}>{f}</option>)}
          </select>
          <button onClick={() => setShowModal(true)}
            style={{ background: "#fff", border: "none", borderRadius: 3, padding: "8px 20px", color: G, fontWeight: 800, fontSize: 13, cursor: "pointer" }}>
            + Nieuwe Prestatie
          </button>
        </div>
      </div>

      {/* 5-column grid */}
      <div style={{ padding: "20px 18px", overflowX: "auto" }}>
        <div style={{ display: "grid", gridTemplateColumns: "repeat(5, minmax(200px, 1fr))", gap: 14, minWidth: 900 }}>
          {CATEGORIES.map(cat => {
            const items = sorted(cat.id);
            return (
              <div key={cat.id} style={{ display: "flex", flexDirection: "column" }}>
                {/* Column header */}
                <div style={{ background: G, color: "#fff", borderRadius: "4px 4px 0 0", padding: "9px 12px", display: "flex", alignItems: "center", gap: 7, minHeight: 52, boxSizing: "border-box" }}>
                  <span style={{ fontSize: 15, flexShrink: 0 }}>{cat.emoji}</span>
                  <span style={{ fontWeight: 800, fontSize: 12, flex: 1, lineHeight: 1.3 }}>{cat.label}</span>
                  <button
                    onClick={() => setInspOpen(inspOpen === cat.id ? null : cat.id)}
                    title="Inspiratie"
                    style={{
                      background: inspOpen === cat.id ? "rgba(255,255,255,0.35)" : "rgba(255,255,255,0.15)",
                      border: "none", borderRadius: 3, padding: "2px 7px", cursor: "pointer",
                      fontSize: 11, color: "#fff", fontWeight: 700, flexShrink: 0, marginRight: 2,
                    }}>
                    💡
                  </button>
                  <span style={{ background: "rgba(255,255,255,0.2)", borderRadius: 10, padding: "1px 7px", fontSize: 11, fontWeight: 700, flexShrink: 0 }}>{items.length}</span>
                </div>

                {/* Inspiratie dropdown */}
                {inspOpen === cat.id && (
                  <div style={{ background: "#FFFDE8", border: `1px solid #E8D84A`, borderTop: "none", padding: "10px 12px" }}>
                    <div style={{ fontSize: 10, fontWeight: 800, color: "#8A7A00", textTransform: "uppercase", letterSpacing: 1, marginBottom: 7 }}>💡 Inspiratie</div>
                    {INSPIRATIE[cat.id].map((tip, i) => (
                      <div key={i} style={{ fontSize: 11, color: "#4A3F00", padding: "4px 0", borderTop: i > 0 ? "1px solid #F0E060" : "none", lineHeight: 1.4 }}>
                        {tip}
                      </div>
                    ))}
                  </div>
                )}

                {/* Cards container */}
                <div style={{ background: "#fff", border: `1px solid ${GB}`, borderTop: "none", borderRadius: "0 0 4px 4px", flex: 1 }}>
                  {items.length === 0 ? (
                    <div style={{ padding: "18px 12px", textAlign: "center", color: "#bbb", fontSize: 12 }}>Nog geen prestaties</div>
                  ) : items.map((item, idx) => {
                    const score = item.thumbsUp.length - item.thumbsDown.length;
                    const hasVoted = false; // voting can always be changed
                    const isOwn = voter === item.name;
                    const medal = idx === 0 && items.length > 1 ? "🥇" : idx === 1 && items.length > 2 ? "🥈" : null;
                    return (
                      <div key={item.id} style={{
                        borderTop: idx > 0 ? `1px solid ${GB}` : "none",
                        padding: "11px 12px",
                        background: idx === 0 && items.length > 1 ? GL : "#fff",
                      }}>
                        {/* Name + score */}
                        <div style={{ display: "flex", justifyContent: "space-between", alignItems: "center", marginBottom: 5 }}>
                          <div style={{ display: "flex", alignItems: "center", gap: 5 }}>
                            {medal && <span style={{ fontSize: 12 }}>{medal}</span>}
                            <span style={{ background: G, color: "#fff", borderRadius: 2, padding: "2px 8px", fontSize: 11, fontWeight: 700 }}>{item.name}</span>
                          </div>
                          <div style={{ display: "flex", alignItems: "center", gap: 6 }}>
                            <span style={{ fontSize: 13, fontWeight: 800, color: score > 0 ? G : score < 0 ? "#B91C1C" : "#bbb" }}>
                              {score > 0 ? "+" : ""}{score}
                            </span>
                            {isOwn && (
                              <button
                                onClick={() => deleteAchievement(item.id)}
                                title="Verwijder mijn prestatie"
                                style={{
                                  background: "none", border: "1px solid #EFCFCF", borderRadius: 3,
                                  padding: "1px 6px", cursor: "pointer", fontSize: 11, color: "#B91C1C",
                                  lineHeight: 1.4, fontWeight: 700,
                                }}>
                                ✕
                              </button>
                            )}
                          </div>
                        </div>

                        {/* Description */}
                        <p style={{ margin: "0 0 9px", fontSize: 12, lineHeight: 1.55, color: "#3A4A3E" }}>{item.description}</p>

                        {/* Buttons */}
                        <div style={{ display: "flex", gap: 5 }}>
                          {[["up", "👍", item.thumbsUp, G, GB], ["down", "👎", item.thumbsDown, "#B91C1C", "#EFCFCF"]].map(([type, icon, arr, ac, bc]) => (
                            <button key={type} onClick={() => vote(item.id, type)}
                              disabled={isOwn || hasVoted}
                              style={{
                                background: arr.includes(voter) ? ac : "#fff",
                                border: `1px solid ${arr.includes(voter) ? ac : bc}`,
                                borderRadius: 3, padding: "4px 9px", cursor: isOwn || hasVoted ? "default" : "pointer",
                                fontSize: 12, color: arr.includes(voter) ? "#fff" : ac,
                                fontWeight: 700, display: "flex", alignItems: "center", gap: 3,
                                opacity: isOwn ? 0.3 : 1,
                                transform: animId === item.id + type ? "scale(1.18)" : "scale(1)",
                                transition: "transform 0.18s",
                              }}>
                              {icon} <span>{arr.length}</span>
                            </button>
                          ))}
                        </div>

                        {/* Voter names */}
                        {(item.thumbsUp.length > 0 || item.thumbsDown.length > 0) && (
                          <div style={{ marginTop: 6, fontSize: 10, color: "#999", lineHeight: 1.5 }}>
                            {item.thumbsUp.length > 0 && <span>👍 {item.thumbsUp.join(", ")}</span>}
                            {item.thumbsUp.length > 0 && item.thumbsDown.length > 0 && " · "}
                            {item.thumbsDown.length > 0 && <span>👎 {item.thumbsDown.join(", ")}</span>}
                          </div>
                        )}
                      </div>
                    );
                  })}
                </div>
              </div>
            );
          })}
        </div>
      </div>

      {/* Modal */}
      {showModal && (
        <div style={{ position: "fixed", inset: 0, background: "rgba(0,0,0,0.4)", display: "flex", alignItems: "center", justifyContent: "center", zIndex: 1000, padding: 20 }}
          onClick={e => e.target === e.currentTarget && setShowModal(false)}>
          <div style={{ background: "#fff", borderRadius: 5, padding: 26, width: "100%", maxWidth: 420, boxShadow: "0 8px 32px rgba(0,0,0,0.18)", border: `1px solid ${GB}`, animation: "pi 0.18s ease" }}>
            <div style={{ display: "flex", justifyContent: "space-between", alignItems: "center", marginBottom: 18 }}>
              <h3 style={{ margin: 0, fontSize: 16, fontWeight: 800, color: G }}>Nieuwe Prestatie</h3>
              <button onClick={() => setShowModal(false)} style={{ background: "none", border: "none", fontSize: 17, cursor: "pointer", color: "#999" }}>✕</button>
            </div>
            <div style={{ display: "flex", flexDirection: "column", gap: 13 }}>
              <div>
                <label style={{ fontSize: 11, fontWeight: 700, color: "#666", textTransform: "uppercase", letterSpacing: 1, display: "block", marginBottom: 4 }}>Naam</label>
                <select value={form.name} onChange={e => setForm(f => ({ ...f, name: e.target.value }))}
                  style={{ width: "100%", background: "#fff", border: `1px solid ${GB}`, borderRadius: 3, padding: "8px 10px", fontSize: 13, color: form.name ? "#1C2B22" : "#999", outline: "none", boxSizing: "border-box" }}>
                  <option value="">Selecteer naam...</option>
                  {FRIENDS.map(f => <option key={f} value={f}>{f}</option>)}
                </select>
              </div>
              <div>
                <label style={{ fontSize: 11, fontWeight: 700, color: "#666", textTransform: "uppercase", letterSpacing: 1, display: "block", marginBottom: 4 }}>Categorie</label>
                <div style={{ display: "flex", flexDirection: "column", gap: 5 }}>
                  {CATEGORIES.map(cat => (
                    <label key={cat.id} style={{ display: "flex", alignItems: "center", gap: 8, padding: "7px 10px", borderRadius: 3, cursor: "pointer", background: form.category === cat.id ? GL : "#FAFAFA", border: `1px solid ${form.category === cat.id ? G : GB}`, transition: "all 0.1s" }}>
                      <input type="radio" name="cat" value={cat.id} checked={form.category === cat.id} onChange={e => setForm(f => ({ ...f, category: e.target.value }))} style={{ accentColor: G }} />
                      <span>{cat.emoji}</span>
                      <span style={{ fontSize: 13, color: form.category === cat.id ? G : "#555", fontWeight: form.category === cat.id ? 700 : 400 }}>{cat.label}</span>
                    </label>
                  ))}
                </div>
              </div>
              <div>
                <label style={{ fontSize: 11, fontWeight: 700, color: "#666", textTransform: "uppercase", letterSpacing: 1, display: "block", marginBottom: 4 }}>Omschrijving</label>
                <textarea value={form.description} onChange={e => setForm(f => ({ ...f, description: e.target.value }))} placeholder="Wat heb je gedaan?" rows={3}
                  style={{ width: "100%", background: "#fff", border: `1px solid ${GB}`, borderRadius: 3, padding: "8px 10px", color: "#1C2B22", fontSize: 13, resize: "vertical", outline: "none", fontFamily: "inherit", boxSizing: "border-box" }} />
              </div>
              <div style={{ display: "flex", gap: 8, marginTop: 2 }}>
                <button onClick={() => setShowModal(false)} style={{ flex: 1, background: "#fff", border: `1px solid ${GB}`, borderRadius: 3, padding: "9px", color: "#666", fontWeight: 700, fontSize: 13, cursor: "pointer" }}>Annuleren</button>
                <button onClick={add} disabled={!form.name || !form.description.trim()}
                  style={{ flex: 2, background: form.name && form.description.trim() ? G : "#ccc", border: "none", borderRadius: 3, padding: "9px", color: "#fff", fontWeight: 800, fontSize: 13, cursor: form.name && form.description.trim() ? "pointer" : "default", transition: "background 0.15s" }}>
                  Toevoegen
                </button>
              </div>
            </div>
          </div>
        </div>
      )}

      <style>{`
        @keyframes sd { from { transform: translateX(-50%) translateY(-10px); opacity: 0; } to { transform: translateX(-50%) translateY(0); opacity: 1; } }
        @keyframes pi { from { transform: scale(0.96); opacity: 0; } to { transform: scale(1); opacity: 1; } }
        select option { background: #fff; color: #1C2B22; }
      `}</style>
    </div>
  );
}
