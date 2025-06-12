
# 🧠 Day 1 – What Are AI Agents?

## 🔍 Konu Özeti

- AI Agents, kullanıcıdan sadece komut değil, **hedef** alır. (AI agents take vague goals and figure out how to achieve them.)
- Agent: “Uçak bileti + otel ayarla” gibi belirsiz bir hedefi gerçekleştirmek için araçlar seçer, plan yapar.
- Workflow: Sabit adımlar izler.
- Agent: Duruma göre araç seçer, adımları kendisi belirler (daha esnek ve akıllı).
- Vellum AI’ye göre otonomi seviyeleri L0–L5 arasında değişir.

---

## 🧱 Otonomi Seviyeleri (Vellum AI)

| Seviye | Rol        | Davranış Açıklaması                       |
|--------|------------|-------------------------------------------|
| L0     | Takipçi     | Sabit kuralları uygular                  |
| L1     | Uygulayıcı  | Komutlara yanıt verir, planlama yapmaz   |
| L2     | Aktör       | Araçları sadece istendiğinde kullanır    |
| L3     | Operatör    | Kendi planını yapar, aksiyonları ayarlar |
| L4     | Otonom      | Hedef koyar, adapte olur                 |
| L5     | Yenilikçi   | Yepyeni çözümler üretir                  |

*Most agents today live in L2–L3 territory. L4+ is where real autonomy starts.
---

## 🌍 Gerçek Hayat Kullanım Alanları

| Alan            | Uygulama Örneği                                |
|-----------------|-------------------------------------------------|
| Sağlık          | Hasta geçmişine göre ilaç önerme               |
| Seyahat         | Uçuş + otel ayarlama                           |
| Satış           | Otomatik müşteri takibi                        |
| Borsa           | Alım-satım işlemleri, piyasa analizi           |
| Destek          | 7/24 müşteri destek sistemi                    |
| Eğitim          | AI destekli rehber öğretmen                    |

---

## 🧰 Agent Framework’leri

| Framework    | Özellikler                                     |
|--------------|-------------------------------------------------|
| LangGraph    | Tracing var, code interpreter yok              |
| Agents SDK   | Tracing ve code interpreter destekli           |
| Mastra       | Temel özellikler, tracing yok                  |
| CrewAI       | Code interpreter destekli ama tracing yok      |

> Eğitim süresince **OpenAI SDK** kullanılacak.

---

## 🧠 LLM Agent'ların Çekirdeği

- **Planlama**: Chain-of-thought ile görev alt parçalara ayrılır.
- **Hafıza**: Kısa ve uzun vadeli içerik takibi (Day 4’te detaylı).
- **Araç Kullanımı**: API, arama, hesap makinesi, vs.

---

## ✍️ Kendi Notlarım

- Agent ile workflow farkını çok net anladım.
- L3 seviyesindeki bir agent Flutter’da oluşturulabilir (özellikle basit planlama + araç kullanımıyla).
- Gerçek hafıza kullanmadan "simülasyonla hafıza" oluşturmak ilginç geldi.
- LangChain ve CrewAI framework'lerini derinlemesine incelemeyi düşünüyorum.
