# 🧪 Mini Experiment Plan: Sentiment Agent – Açıklamalı Versiyon

## 🎯 Hedef
Kullanıcının yazdığı duygu içeren bir cümleyi analiz eden, buna uygun yanıt üreten ve bu süreci hafifçe “hafızayla zenginleştiren” basit bir AI agent deneyimi oluşturmak.

> Bu mini proje, “agent” kavramını Flutter’da nasıl uygulayabileceğini deneyimlemene olanak sağlar.

---

## 🧱 Adımların Detaylı Açıklaması

### 1. Prompt user for input
- Kullanıcıdan basit bir duygu ifadesi alınır.
- Örnek: `"I'm feeling unmotivated today."`
- Flutter’da bir `TextField` + `Submit` butonu ile yapılabilir.

---

### 2. Use TFLite or API to detect sentiment
Kullanıcının yazdığı cümledeki **duygu analizi** yapılır:

#### Offline çözüm:
- Önceden eğitilmiş bir sentiment analiz modelini `.tflite` formatında Flutter’a entegre et.

#### Online çözüm:
- Flask veya FastAPI ile backend kurulur, model Python tarafında çalıştırılır.

**Çıktı:** `"Negative"`, `"Positive"`, `"Neutral"` gibi etiketler.

---

### 3. Agent replies with a motivational quote or advice
Agent, duygunun türüne göre uygun ve motive edici yanıt verir:

> `"You’re not alone. Take a short walk and breathe — you got this 💪"`

- Yanıtlar:
  - Sabit olarak tanımlanabilir
  - Ya da LLM (örn. OpenAI, Gemini) ile üretilebilir

---

### 4. Log interaction memory (simulated memory concept)
Agent-like davranış için “hafıza” simülasyonu ekle:

- Önceki duygu ve yanıtları bir `List` içinde sakla.
- Yeni gelen duyguya göre geçmişe referans vererek yanıt üret.

**Örnek:**
User: I'm sad again today.
Agent: I remember you were down yesterday too. Let’s try a new strategy today: write 3 things you’re grateful for. 🙏

🧠 Bu gerçek hafıza değil ama **agent davranışı taklidi** olarak güçlü bir etkidir.

---

## 🚀 Stretch Goal – Follow-up Interactions with Memory

- **Amaç:** Kullanıcının geçmiş duygu durumlarını izleyip, uzun vadeli strateji önermek.

> Örnek: 3 gün üst üste olumsuz hisseden kullanıcıya:  
> `"Would you like to talk to someone?"`

### Teknik Yaklaşım:

- Basit bir `List<Map<String, String>>` yapısıyla tarih–duygu eşleşmelerini sakla.
- Günlük yorum geldiğinde bu listeyi değerlendirerek ajan yanıtını daha akıllı hale getir.

---

## 🎁 Bu Proje Neyi Öğretir?

| Öğrenim Alanı       | Ne Öğrenirsin                               |
|---------------------|----------------------------------------------|
| **Flutter UI/UX**   | Form, yanıt UI, async yapı                   |
| **AI Agents**       | Planlama, hafıza simülasyonu, tepki üretme   |
| **NLP / ML**        | Sentiment analizi entegrasyonu               |
| **MLOps**           | TFLite ya da API ile model deploy etme       |

---

## 📁 Önerilen Dosya Yapısı

```plaintext
lib/
├── ui/
│   └── input_form.dart
├── agent.dart
├── memory_store.dart
├── sentiment_model.dart  # (isteğe bağlı)

---
