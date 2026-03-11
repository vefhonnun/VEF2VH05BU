Hér er uppfærð útgáfa af skránni með íslenskri þýðingu **fyrir ofan** enska textann:
# HTML role -eigindið

---

**role-eigindið** í HTML veitir tögum merkingarfræðilega þýðingu, sérstaklega ósérhæfðum tögum eins og `<div>` eða `<span>`, og hjálpar hjálpartækjum (eins og skjálesurum) að skilja tilgang og virkni tags. Það er hluti af WAI-ARIA (Web Accessibility Initiative - Accessible Rich Internet Applications) staðlinum, sem bætir aðgengi fyrir notendur með fötlun.

### **Tilgangur og virkni**
- **Merkingarfræðilegur skýrleiki**: Innbyggðir HTML-þættir (t.d. `<button>`, `<nav>`, `<a>`) hafa innbyggð hlutverk (t.d. `button`, `navigation`). `role` eigindið er notað til að skilgreina hlutverk almennra þátta sérstaklega þegar þeir eru notaðir sem gagnvirkir eða byggingarlegir þættir.
- **Stuðningur við aðgengi**: Skjálesarar nota `role` eigindið til að lesa þætti rétt. Til dæmis er `<div role="button">` lesið sem „button“ í stað almenns „div“ eða „link“.
- **Varahlutverk og staðfesting**: Eigindið getur tekið mörg bilskilin gildi (varahlutverk). Fyrsta gilda ARIA-hlutverkið í listanum er notað. Ógild eða óhlutbundin hlutverk eru hunsuð.

### **Algeng ARIA-hlutverk**
| Hlutverk | Tilgangur |
|------|--------|
| `button` | Merk­ir þátt sem smellanlegan hnapp |
| `navigation` | Skilgreinir leiðsagnarsvæði |
| `alert` | Tilkynnir brýn skilaboð strax |
| `region` | Hópar tengt efni til að auðvelda leiðsögn |
| `dialog` | Auðkennir gluggakassa (modal dialog) |
| `main` | Merk­ir aðalefni skjals |

### **Bestu starfsvenjur**
- **Kjósa innbyggða HTML-þætti** þegar hægt er (t.d. nota `<button>` í stað `<div role="button">`).
- **Bæta við lyklaborðsstuðningi** (t.d. `tabindex="0"`, meðhöndlun á `Enter`/`Space`) fyrir gagnvirk hlutverk.
- **Forðast óhlutbundin hlutverk** (t.d. `widget`, `command`) — þau eru ekki ætluð til beinnar notkunar af forriturum.
- **Prófa með mörgum skjálesurum** (t.d. NVDA, JAWS, VoiceOver) til að tryggja rétta hegðun.

### **Mikilvæg atriði**
- `role` eigindið bætir ekki við virkni — það miðlar aðeins merkingu.
- Röng eða óþörf notkun getur ruglað notendur og dregið úr aðgengi.
- Rétt notkun hjálpar til við að uppfylla WCAG 2.1 viðmið eins og **1.3.1 (Upplýsingar og tengsl)** og **4.1.2 (Nafn, hlutverk, gildi)**.

Rétt notkun `role` eigindisins tryggir að vefefni sé meira inngildandi og nothæft fyrir fólk sem treystir á hjálpartækni.

---

# HTML Role Attribute

---

The **role attribute** in HTML provides semantic meaning to elements, especially non-semantic ones like `<div>` or `<span>`, helping assistive technologies (such as screen readers) understand the purpose and function of an element. It is part of the WAI-ARIA (Web Accessibility Initiative - Accessible Rich Internet Applications) specification, which enhances accessibility for users with disabilities.

### **Purpose and Function**
- **Semantic Clarity**: Native HTML elements (e.g., `<button>`, `<nav>`, `<a>`) have built-in roles (e.g., `button`, `navigation`). The `role` attribute is used to explicitly define the role of generic elements when they are used to represent interactive or structural components.
- **Accessibility Support**: Screen readers use the `role` attribute to announce elements correctly. For example, a `<div role="button">` is read as "button" instead of a generic "div" or "link".
- **Fallback and Validation**: The attribute can accept multiple space-separated values (fallback roles). The first valid ARIA role in the list is used. Invalid or abstract roles are ignored.

### **Common ARIA Roles**
| Role | Purpose |
|------|--------|
| `button` | Marks an element as a clickable button |
| `navigation` | Defines a navigational region |
| `alert` | Announces urgent messages immediately |
| `region` | Groups related content for easier navigation |
| `dialog` | Identifies a modal dialog window |
| `main` | Indicates the primary content of a document |

### **Best Practices**
- **Prefer native HTML elements** when possible (e.g., use `<button>` instead of `<div role="button">`).
- **Add keyboard support** (e.g., `tabindex="0"`, `Enter`/`Space` key handling) for interactive roles.
- **Avoid abstract roles** (e.g., `widget`, `command`) — they are not meant for direct use by developers.
- **Test with multiple screen readers** (e.g., NVDA, JAWS, VoiceOver) to ensure proper behavior.

### **Key Considerations**
- The `role` attribute does not add functionality — it only communicates semantics.
- Incorrect or redundant use can confuse users and degrade accessibility.
- It helps meet WCAG 2.1 success criteria such as **1.3.1 (Info and Relationships)** and **4.1.2 (Name, Role, Value)**.

Using the `role` attribute correctly ensures that web content is more inclusive and usable for people relying on assistive technologies.

