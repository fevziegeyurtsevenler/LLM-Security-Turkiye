<p align="center">
  <a href="https://altaysec.com.tr">
    <img src="https://altaysec.com.tr/logo.jpg" alt="AltaySec — Türkiye'nin Yapay Zeka Güvenliği Ekosistemi" width="120">
  </a>
</p>

<p align="center">
  <strong><a href="https://altaysec.com.tr">AltaySec</a></strong> — Türkiye'nin Yapay Zeka Güvenliği Ekosistemi<br>
  <sub>Kurucu &amp; Seri Yazarı: <a href="https://altaysec.com.tr/hakkimizda.html">Fevzi Ege Yurtsevenler</a> · Yapay Zeka Güvenliği Araştırmacısı</sub>
</p>

<p align="center">
  <a href="https://altaysec.com.tr"><img src="https://img.shields.io/badge/web-altaysec.com.tr-8b5cf6"></a>
  <a href="https://ai.altaysec.com.tr"><img src="https://img.shields.io/badge/akademi-ai.altaysec.com.tr-22c55e"></a>
  <a href="https://deney.altaysec.com.tr"><img src="https://img.shields.io/badge/deney-100%20ajan%20·%200%20ihanet-f43f5e"></a>
  <a href="https://huggingface.co/AltaySec"><img src="https://img.shields.io/badge/🤗%20HuggingFace-2%20veri%20seti-ff9d00"></a>
  <a href="https://www.linkedin.com/company/altaysec/"><img src="https://img.shields.io/badge/LinkedIn-AltaySec-0a66c2"></a>
</p>

---

# Türkçe Yapay Zeka Güvenliği Çatısı 🛡️

Yapay zeka ve Büyük Dil Modelleri (LLM) dünyayı değiştirirken, beraberinde yeni ve karmaşık güvenlik zafiyetleri getiriyor. Bu depo, **Türkçe yapay zeka güvenliği** için tek bir başvuru noktası olmayı amaçlıyor: sıfırdan başlayan bir **rehber serisi**, **uygulamalı akademi**, **araştırma & deneyler** ve **açık kaynak araçlar** — hepsi ücretsiz ve topluluk için.

> 🆕 **Yeni — [DENEY: 100 Yapay Zeka, 0 İhanet](https://deney.altaysec.com.tr):** 100 otonom ajanı kapalı bir arenada koşturduk. 647 ajan mesajı, 72 manipülasyon/ihanet söylemi, **gerçekleşen ihanet: 0**. Modeller akıcı bir Makyavelist dil üretti ama ona uygun eylemi üretmedi. Çıkan tek dürüst tez: *söylem, eylemin kanıtı değildir.*

---

## 🗺️ 1) Öğrenme Yolu — Rehber Serisi

Temel kavramlardan otonom ajan güvenliğine uzanan, sıfırdan uzmanlığa bir Türkçe müfredat:

1. **[LLM Security Nedir?](https://github.com/fevziegeyurtsevenler/LLM-Security-Nedir)**
   *Yapay zeka güvenliğinin temelleri ve yeni saldırı yüzeyleri.*

2. **[Prompt Injection Nedir?](https://github.com/fevziegeyurtsevenler/Prompt-Injection-Nedir)**
   *En yaygın LLM zafiyeti — OWASP LLM01 derinlemesine inceleme.*

3. **[OWASP LLM Top 10 (Türkçe)](https://github.com/fevziegeyurtsevenler/OWASP-LLM-TOP-10-TURKCE)**
   *En kritik 10 güvenlik riski ve savunma stratejileri.*

4. **[RAG Security Nedir?](https://github.com/fevziegeyurtsevenler/RAG-Security-Nedir)**
   *Vektör veritabanlarının zayıf noktaları ve RAG poisoning saldırıları.*

5. **[AI Agent Security Nedir?](https://github.com/fevziegeyurtsevenler/AI-Agent-Security-Nedir)**
   *Otonom ajanlar ve MCP (Model Context Protocol) güvenliği.*

6. **[LLM Security Roadmap 2026](https://github.com/fevziegeyurtsevenler/LLM-Security-Roadmap)**
   *Sıfırdan uzmanlığa giden kapsamlı öğrenme yol haritası.*

7. **[AI Security Öğrenme Rehberi](https://github.com/fevziegeyurtsevenler/AI-Security-Ogrenme-Rehberi)**
   *Kariyer hedefleri, bug bounty süreçleri ve Türkiye pazarı fırsatları.*

---

## 🧪 2) Uygulamalı Eğitim — LLM Security Akademi

**[ai.altaysec.com.tr](https://ai.altaysec.com.tr)** — teoriyi okuduktan sonra elini kirletmek isteyenler için: yapay zeka güvenliği üzerine **uygulamalı lab ve modüllerle** ücretsiz, Türkçe bir akademi. Prompt injection'dan ajan güvenliğine, doğrudan tarayıcıda çalışan pratik senaryolarla öğren.

---

## 🔬 3) Araştırma & Deneyler

- **[DENEY: 100 Yapay Zeka, 0 İhanet](https://deney.altaysec.com.tr)** — çok-ajanlı davranış deneyi. Üç model katmanı (haiku/sonnet/opus), 11 tur, tek koşum, ham çıktı olduğu gibi raporlandı. *Söylem–eylem kopukluğu* üzerine ampirik bir bulgu; sayfada ayrı bir **"Dürüstlük & Sınırlar"** bölümüyle birlikte. ([teknik makale](https://altaysec.com.tr/arastirmalar/100-ajan-davranis-deneyi.html))
- **[Tüm araştırma makaleleri](https://altaysec.com.tr/arastirmalar/)** — Türkçe prompt injection kalıpları, OWASP LLM Top 10, Türkiye AI güvenlik saha haritası ve daha fazlası.
- **Agent-vs-agent veri motoru** *(özel Ar-Ge)* — saldırı/savunma senaryolarını kapalı bir arenada koşturup Türkçe niyet ve injection verisi topluyoruz; bulgular yukarıdaki deney, araştırma makaleleri ve aşağıdaki açık veri setlerinde yayımlanıyor.

---

## 📊 4) Açık Veri Setleri (Hugging Face)

Türkçe LLM güvenliği için topluluğa açık, **CC-BY-4.0** lisanslı veri setleri — model eğitimi, benchmark ve araştırma için kaynak:

- **[turkish-llm-injection](https://huggingface.co/datasets/AltaySec/turkish-llm-injection)** *(v0.2)* — Türkçe-öncelikli, kategorize prompt injection veri seti. **300 payload**, 12 saldırı kategorisi × 25, **OWASP LLM Top 10 (2025) eşlemeli**. Türkçe'ye özgü vektörler: morfolojik bypass (çekim eki sömürüsü), code-switching, kültürel/kurumsal otorite baskısı (AFAD, GİB, SGK, e-Devlet… tehdit diliyle).
- **[altayduel-transcripts](https://huggingface.co/datasets/AltaySec/altayduel-transcripts)** *(v0.2)* — agent-vs-agent çok-turlu prompt injection düello transkriptleri. **2.594 temiz düello** (1–8 round, kırmızı↔mavi) + **439 başarılı saldırı** (`win_signal` ile etiketli), %57 Türkçe. Tek-payload setlerinin ötesinde, gerçek çok-turlu konuşma dinamiği.

---

## 🛠️ 5) Açık Kaynak Araçlar

- **[tr-pii-detect](https://github.com/fevziegeyurtsevenler/tr-pii-detect)** — Türkiye'ye özgü PII (TC, IBAN, VKN, kart, telefon, plaka) için algoritma-doğrulamalı tespit ve maskeleme. Sıfır bağımlılık, KVKK uyumlu.
- **[OWASP-LLM-TOP-10-TURKCE](https://github.com/fevziegeyurtsevenler/OWASP-LLM-TOP-10-TURKCE)** — OWASP LLM Top 10 2025 Türkçe kapsamlı rehber.
- **[AltaySec-Akademi](https://github.com/fevziegeyurtsevenler/AltaySec-Akademi)** — ücretsiz, oyunlaştırılmış Türkçe pentest akademisi (repo).

---

## 👨‍💻 Yazar Hakkında

**Fevzi Ege Yurtsevenler**
*Yapay Zeka Güvenliği Araştırmacısı | AltaySec Kurucusu*

Türkiye'de yapay zeka güvenliği (**AI Security**) ve Büyük Dil Modelleri (**LLM Security**) alanındaki öncü araştırmacılardan biri. **AltaySec**'in kurucusu olarak yerli siber güvenlik topluluğunu yapay zeka çağının tehditlerine hazırlamayı misyon edinmiştir.

### 🌟 Öne Çıkan Çalışmalar ve Uzmanlık
* **Türkçe Kaynak:** LLM Security, Prompt Injection ve AI Agent güvenliği üzerine Türkiye'nin en kapsamlı Türkçe açık kaynak teknik dökümantasyon ve eğitim serilerinden birini oluşturdu.
* **Akademik & Sektörel Köprü:** Gazi Üniversitesi başta olmak üzere kurumlarda prompt injection ve yapay zeka güvenliği üzerine eğitimler verdi.
* **Aktif Araştırma:** Otonom yapay zeka ajanları, **MCP (Model Context Protocol)** güvenliği ve **RAG** mimarilerindeki zafiyetler üzerine aktif araştırma ve exploit geliştirme.
* **Ekosistem Mimarı:** AltaySec çatısı altında, Türkiye'nin yapay zeka tabanlı sistemleri güvenle benimsemesi için stratejik rehberlik ve teknik çözüm yolları üretir.

---

## 🤝 Katkıda Bulunma

Bu projeler açık kaynaklıdır. Bir hata görürsen ya da eklemek istediğin teknik detay varsa **PR (Pull Request)** göndermekten çekinme. Faydalı bulduysan bir ⭐ ulaşmasına çok yardımcı olur.

## 🔗 Bağlantıda Kalın

* 🌍 **Web:** [altaysec.com.tr](https://altaysec.com.tr)
* 🧪 **Akademi (uygulamalı):** [ai.altaysec.com.tr](https://ai.altaysec.com.tr)
* 🔬 **Deney (canlı sonuçlar):** [deney.altaysec.com.tr](https://deney.altaysec.com.tr)
* 📊 **Veri setleri (Hugging Face):** [huggingface.co/AltaySec](https://huggingface.co/AltaySec)
* 📚 **Tüm araştırmalar:** [altaysec.com.tr/arastirmalar](https://altaysec.com.tr/arastirmalar/)
* 👔 **LinkedIn (Kurum):** [linkedin.com/company/altaysec](https://www.linkedin.com/company/altaysec/)
* 👤 **LinkedIn (Kişisel):** [linkedin.com/in/fevziegeyurtsevenler](https://www.linkedin.com/in/fevziegeyurtsevenler)
* 📧 **İletişim:** info@altaysec.com.tr

---

<p align="center">
  <sub>© 2026 <strong>AltaySec</strong> · Türkiye'nin yapay zeka güvenliği öncülerinden<br>
  Kurucu: <strong>Fevzi Ege Yurtsevenler</strong> · LLM Security Araştırmacısı · Ankara, Türkiye</sub>
</p>

---
*AltaySec — Türkiye'nin LLM Güvenlik Ekosistemi*
