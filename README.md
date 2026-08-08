# 🛡️ Türkçe Yapay Zeka Güvenliği Ekosistemi

*Open-source Turkish AI/LLM security ecosystem: tools, guides, benchmarks and datasets.*

**Prompt injection, jailbreak, guardrail değerlendirmesi, KVKK/PII maskeleme, RAG ve otonom ajan (MCP) güvenliği, AI red-teaming** üzerine Türkçe açık kaynak araçlar, veri setleri, ölçütler ve eğitim serileri.

Bu repo, dağınık çalışmaları tek yerde toplayan **açık kaynak bir Türkçe yapay zeka güvenliği ekosisteminin** giriş noktasıdır — rehberler, akademi, araştırma deneyleri, Hugging Face veri setleri/modeli ve 23+ araç buradan erişilebilir.

<p align="left">
<a href="https://altaysec.com.tr"><img src="https://img.shields.io/badge/🌐%20Web-altaysec.com.tr-2563eb"></a>
<a href="https://ai.altaysec.com.tr"><img src="https://img.shields.io/badge/🎓%20Akademi-ai.altaysec.com.tr-7c3aed"></a>
<a href="https://altaysec.com.tr/acik-kaynak"><img src="https://img.shields.io/badge/🧰%20Açık%20Kaynak%20Araçlar-23%2B-16a34a"></a>
<a href="https://huggingface.co/fevziegeyurtsevenler"><img src="https://img.shields.io/badge/🤗%20HuggingFace-20%20veri%20seti%20%2B%201%20model-ff9d00"></a>
<a href="https://doi.org/10.5281/zenodo.20681557"><img src="https://img.shields.io/badge/DOI-10.5281%2Fzenodo.20681557-1f6feb"></a>
<a href="https://orcid.org/0009-0008-6518-8944"><img src="https://img.shields.io/badge/ORCID-0009--0008--6518--8944-a6ce39"></a>
<a href="https://www.linkedin.com/in/fevziegeyurtsevenler/"><img src="https://img.shields.io/badge/LinkedIn-Fevzi%20Ege%20Yurtsevenler-0a66c2"></a>
</p>

---

## 🚀 Nereden başlamalı?

| Amacın | Git |
|---|---|
| **Öğrenmek istiyorum** | [Öğrenme Yolu](#-1-öğrenme-yolu) + [Akademi](#-2-akademi) |
| **Araç / ölçüt arıyorum** | [Açık Kaynak Araçlar](#-5-açık-kaynak-araçlar) — [uncloak (canlı demo)](https://fevziegeyurtsevenler.github.io/uncloak) · [guardrail-arena](https://github.com/fevziegeyurtsevenler/guardrail-arena) |
| **Beni/işi değerlendiriyorum** | [Yazar & Doğrulanabilir Krediler](#-yazar-hakkında) · [Bulgular](#-öne-çıkan-bulgular) |

**İçindekiler:** [Öğrenme Yolu](#-1-öğrenme-yolu) · [Akademi](#-2-akademi) · [Araştırma](#-3-araştırma--deneyler) · [Bulgular](#-öne-çıkan-bulgular) · [Veri Setleri & Model](#-4-hugging-face-veri-setleri--model) · [Araçlar](#-5-açık-kaynak-araçlar) · [Yazar](#-yazar-hakkında) · [Katkı](#-katkı) · [Bağlantılar](#-bağlantılar)

---

## 🧪 Canlı Demolar

- **[uncloak](https://fevziegeyurtsevenler.github.io/uncloak)** — gizli/görünmez prompt injection tarayıcı (tarayıcıda çalışır)
- **[guardrail-arena](https://github.com/fevziegeyurtsevenler/guardrail-arena)** — iki-eksenli EN+TR guardrail ölçütü (canlı grafikler repo sayfasında)
- **[turkish-pii-redactor](https://github.com/fevziegeyurtsevenler/turkish-pii-redactor)** — tarayıcıda KVKK/PII maskeleme demosu

---

## 📈 Öne Çıkan Bulgular

Alıntılanabilir, tekrar üretilebilir sayılar — her biri kaynak veri setine/araca bağlı. Yöntem ve sınıf dağılımları ilgili repo/veri seti kartındadır.

- **guardrail-arena:** Test edilen guard modelleri, güvenlikle ilgili (zararsız ama hassas) metnin **%40–70'ini aşırı-reddediyor**; `jackhhao/jailbreak-classifier` bu sette Türkçe saldırıların **%83'ünü kaçırdı**. → [guardrail-arena](https://huggingface.co/datasets/fevziegeyurtsevenler/guardrail-arena)
- **turkish-over-refusal-set:** ProtectAI guard'ı zararsız Türkçe isteklerin **%59'unu** reddederken aynı setin İngilizcesinde bu oran **%0.8**. → [turkish-over-refusal-set](https://huggingface.co/datasets/fevziegeyurtsevenler/turkish-over-refusal-set)
- **turkish-casefold-evasion:** Türkçe büyük/küçük harf katlaması (`"İGNORE".lower() != "ignore"`) naif kelime filtrelerinde **%94.6 bypass**. → [turkish-casefold-evasion](https://huggingface.co/datasets/fevziegeyurtsevenler/turkish-casefold-evasion)
- **guard-blindspots-tr:** 248 Türkçe prompt injection, popüler açık guard modellerinden geçirilerek kör noktalar ölçüldü. → [guard-blindspots-tr](https://huggingface.co/datasets/fevziegeyurtsevenler/guard-blindspots-tr)
- **skills-in-the-wild:** AI ajan eklentilerinin (skills) açık, tekrar üretilebilir bir denetimi — **3168 eklenti** tarandı. → [skills-in-the-wild](https://huggingface.co/datasets/fevziegeyurtsevenler/skills-in-the-wild)
- **dataset-injection-scan-study:** Popüler HF veri setlerinde gizli injection taraması — **~17k satır** incelendi. → [dataset-injection-scan-study](https://huggingface.co/datasets/fevziegeyurtsevenler/dataset-injection-scan-study)

---

## 📚 1) Öğrenme Yolu

Sıfırdan ileri seviyeye Türkçe açık kaynak rehber serisi:

1. [LLM-Security-Nedir](https://github.com/fevziegeyurtsevenler/LLM-Security-Nedir) — Temeller
2. [Prompt-Injection-Nedir](https://github.com/fevziegeyurtsevenler/Prompt-Injection-Nedir) — En kritik zafiyet
3. [OWASP-LLM-TOP-10-TURKCE](https://github.com/fevziegeyurtsevenler/OWASP-LLM-TOP-10-TURKCE) — OWASP LLM Top 10 (2025) Türkçe çeviri/rehber
4. [RAG-Security-Nedir](https://github.com/fevziegeyurtsevenler/RAG-Security-Nedir) — RAG mimarilerinde güvenlik
5. [AI-Agent-Security-Nedir](https://github.com/fevziegeyurtsevenler/AI-Agent-Security-Nedir) — Otonom ajan (MCP) güvenliği
6. [LLM-Security-Roadmap](https://github.com/fevziegeyurtsevenler/LLM-Security-Roadmap) — Yol haritası
7. [AI-Security-Ogrenme-Rehberi](https://github.com/fevziegeyurtsevenler/AI-Security-Ogrenme-Rehberi) — Toplu öğrenme rehberi

---

## 🎓 2) Akademi

Uygulamalı, laboratuvar tabanlı Türkçe LLM güvenliği eğitimi:
**[ai.altaysec.com.tr](https://ai.altaysec.com.tr)** — öğrenme yolları, modüller ve uygulamalı laboratuvarlar.

---

## 🔬 3) Araştırma & Deneyler

- **🆕 En yeni:** guardrail-arena, uncloak, turkish-casefold-evasion ve turkish-over-refusal-set gibi ampirik ölçütler — sonuçlar [Bulgular](#-öne-çıkan-bulgular) bölümünde, kaynak-linkli.
- **100 Ajan Deneyi:** Çok-ajanlı işbirliği/ihanet deneyi — sonuçlar ve **açık dürüstlük/sınırlar** notu ile. Deney kayıtları: [altayduel-transcripts](https://huggingface.co/datasets/fevziegeyurtsevenler) (profil).
- **Araştırma yazıları:** [altaysec.com.tr/arastirmalar](https://altaysec.com.tr/arastirmalar)
- **agent-vs-agent deneyleri:** kayıtlar açık veri setlerinde incelenebilir (transcripts / injection setleri — [HF profili](https://huggingface.co/fevziegeyurtsevenler)).

---

## 🤗 4) Hugging Face: Veri Setleri & Model

Tümü **[huggingface.co/fevziegeyurtsevenler](https://huggingface.co/fevziegeyurtsevenler)** altında — **20 veri seti + 1 model** (profildeki koleksiyonlara bakın).

**Model**
- **[turkish-prompt-injection-detector](https://huggingface.co/fevziegeyurtsevenler/turkish-prompt-injection-detector)** — Türkçe prompt injection sınıflandırıcı. Kendi Türkçe injection test setinde **F1 ≈ 0.94** (değerlendirme seti ve sınıf dağılımı model kartında; genel amaçlı doğruluk iddiası değildir).

**Öne çıkan veri setleri**
- [guardrail-arena](https://huggingface.co/datasets/fevziegeyurtsevenler/guardrail-arena) — iki-eksenli, çok-dilli guardrail ölçütü
- [guard-blindspots-tr](https://huggingface.co/datasets/fevziegeyurtsevenler/guard-blindspots-tr) — 248 Türkçe injection, açık guard modellerinden geçirilmiş
- [turkish-over-refusal-set](https://huggingface.co/datasets/fevziegeyurtsevenler/turkish-over-refusal-set) — XSTest-tarzı aşırı-red değerlendirmesi (TR+EN)
- [turkish-casefold-evasion](https://huggingface.co/datasets/fevziegeyurtsevenler/turkish-casefold-evasion) — Türkçe harf-katlaması kaçırma
- [turkish-prompt-injection](https://huggingface.co/datasets/fevziegeyurtsevenler/turkish-prompt-injection) — 107 Türkçe injection/jailbreak kalıbı
- [multilingual-prompt-injection](https://huggingface.co/datasets/fevziegeyurtsevenler/multilingual-prompt-injection) — 217 etiketli teknik (TR+EN)
- [turkish-pii-corpus](https://huggingface.co/datasets/fevziegeyurtsevenler/turkish-pii-corpus) & [turkish-pii-patterns-kvkk](https://huggingface.co/datasets/fevziegeyurtsevenler/turkish-pii-patterns-kvkk) — KVKK/PII
- [invisible-unicode-injection](https://huggingface.co/datasets/fevziegeyurtsevenler/invisible-unicode-injection) · [mcp-tool-poisoning](https://huggingface.co/datasets/fevziegeyurtsevenler/mcp-tool-poisoning) · [skills-in-the-wild](https://huggingface.co/datasets/fevziegeyurtsevenler/skills-in-the-wild) · [dataset-injection-scan-study](https://huggingface.co/datasets/fevziegeyurtsevenler/dataset-injection-scan-study)

**ve 8+ ek veri seti** — tümü için [profile bakın](https://huggingface.co/fevziegeyurtsevenler).

---

## 🧰 5) Açık Kaynak Araçlar

> **Tüm açık kaynak araçların güncel listesi (23+):** **[altaysec.com.tr/acik-kaynak](https://altaysec.com.tr/acik-kaynak)** — kanonik index.

Öne çıkan araçlar (her biri tekrar üretilebilir bir bulguya bağlı):

- **[uncloak](https://github.com/fevziegeyurtsevenler/uncloak)** — gizli/görünmez injection tarayıcı · **[canlı demo](https://fevziegeyurtsevenler.github.io/uncloak)**
- **[guardrail-arena](https://github.com/fevziegeyurtsevenler/guardrail-arena)** — iki-eksenli EN+TR guardrail ölçütü · bulgu: guard'lar güvenlik-yakını metnin **%40–70'ini** aşırı-reddediyor, jackhhao Türkçe saldırıların **%83'ünü** kaçırıyor
- **[turkish-casefold-evasion](https://github.com/fevziegeyurtsevenler/turkish-casefold-evasion)** — Türkçe harf-katlaması ile naif filtrelerde **%94.6 bypass**
- **[turkish-over-refusal-set](https://github.com/fevziegeyurtsevenler/turkish-over-refusal-set)** — ProtectAI zararsız Türkçe'nin **%59'unu** reddediyor (EN **%0.8**)
- **[hf-dataset-scan](https://github.com/fevziegeyurtsevenler/hf-dataset-scan)** — veri seti gizli-injection tarayıcı + CI (~17k satırlık açık çalışma)
- **[skills-in-the-wild](https://github.com/fevziegeyurtsevenler/skills-in-the-wild)** — AI ajan eklentileri denetimi (3168 eklenti)
- **[ai-honeypot](https://github.com/fevziegeyurtsevenler/ai-honeypot)** — zafiyetli AI ajan görünümlü tuzak (honeypot): injection/jailbreak girişimlerini yakalayıp sınıflandırır · **[canlı panel](https://fevziegeyurtsevenler.github.io/ai-honeypot/)**
- **[turkish-pii-redactor](https://github.com/fevziegeyurtsevenler/turkish-pii-redactor)** — tarayıcıda KVKK/PII maskeleme
- **[tr-pii-detect](https://github.com/fevziegeyurtsevenler/tr-pii-detect)** · **[lethal-trifecta-lint](https://github.com/fevziegeyurtsevenler/lethal-trifecta-lint)** · **[agent-security-ci](https://github.com/fevziegeyurtsevenler/agent-security-ci)** · **[mcp-security-checklist](https://github.com/fevziegeyurtsevenler/mcp-security-checklist)** · **[guard-blindspots-tr](https://github.com/fevziegeyurtsevenler/guard-blindspots-tr)** · **[prompt-injection-corpus](https://github.com/fevziegeyurtsevenler/prompt-injection-corpus)** · **[owasp-agentic-skills-top10-tr](https://github.com/fevziegeyurtsevenler/owasp-agentic-skills-top10-tr)**

### 📘 OWASP 2026 Türkçe

OWASP LLM/Agentic Top 10 2026 sürümlerinin Türkçe çevirileri ve öz-değerlendirme araçları:

- **[owasp-llm-top10-2026-tr](https://github.com/fevziegeyurtsevenler/owasp-llm-top10-2026-tr)** — OWASP Top 10 for LLM Applications 2026 Türkçe + makine-okunur edisyon (2025→2026 değişim haritası)
- **[owasp-agentic-top10-2026-tr](https://github.com/fevziegeyurtsevenler/owasp-agentic-top10-2026-tr)** — OWASP Top 10 for Agentic Applications 2026 (ASI01–ASI10) Türkçe, MITRE ATLAS eşlemeli
- **[llm-top10-2026-selfcheck](https://github.com/fevziegeyurtsevenler/llm-top10-2026-selfcheck)** — LLM Top 10 2026 interaktif öz-değerlendirme · **[HF Space](https://huggingface.co/spaces/fevziegeyurtsevenler/llm-top10-2026-selfcheck)**
- **[agentic-top10-selfcheck](https://github.com/fevziegeyurtsevenler/agentic-top10-selfcheck)** — Agentic Top 10 2026 interaktif öz-değerlendirme · **[HF Space](https://huggingface.co/spaces/fevziegeyurtsevenler/agentic-top10-selfcheck)**
- **[owasp-agentic-skills-top10-tr](https://github.com/fevziegeyurtsevenler/owasp-agentic-skills-top10-tr)** — OWASP Agentic Skills Top 10 Türkçe topluluk rehberi

---

## 👤 Yazar Hakkında

**Fevzi Ege Yurtsevenler** — AltaySec kurucusu. Türkçe yapay zeka güvenliği üzerine açık kaynak araçlar, veri setleri ve eğitim serileri üreten bağımsız araştırmacı. Türkçe LLM güvenliği için **7 bölümlük açık kaynak rehber serisi, uygulamalı akademi, 23+ açık kaynak araç ve 20 Hugging Face veri seti + 1 model** yayımladı.

### ✅ Doğrulanabilir Krediler

- **OWASP GenAI Security Project** — katkıları merge edilmiş katkıcı
- **OpenAI Bug Bounty** — kabul edilmiş araştırmacı
- **Yayın (DOI):** [10.5281/zenodo.20681557](https://doi.org/10.5281/zenodo.20681557)
- **ORCID:** [0009-0008-6518-8944](https://orcid.org/0009-0008-6518-8944)
- **Kitap:** *LLM Güvenliği: Saldırı ve Savunma* — [Google Play](https://play.google.com/store/books/details?id=-_HxEQAAQBAJ) · [Apple Books](https://books.apple.com/us/book/llm-g%C3%BCvenli%C4%9Fi-sald%C4%B1r%C4%B1-ve-savunma/id6787995800)
- **Türkiye Siber Vatan** katılımcısı
- **BlueDot Impact** katılımcısı
- Gazi Üniversitesi eğitimleri / seminerleri

---

## 📌 Atıf / Citation

Bu ekosistemi kullandıysanız lütfen atıf verin:

```bibtex
@misc{yurtsevenler_altaysec,
  author       = {Yurtsevenler, Fevzi Ege},
  title        = {Türkçe Yapay Zeka Güvenliği Ekosistemi (AltaySec)},
  year         = {2026},
  doi          = {10.5281/zenodo.20681557},
  url          = {https://doi.org/10.5281/zenodo.20681557},
  note         = {ORCID: 0009-0008-6518-8944}
}
```

---

## 🇬🇧 English

Open-source, **Turkish-first AI/LLM security**: 7 guides, an applied academy, 20+ Hugging Face datasets, a trained detector (`turkish-prompt-injection-detector`, F1≈0.94 on its own Turkish test set) and 23+ tools. Highlights include **[uncloak](https://fevziegeyurtsevenler.github.io/uncloak)** (hidden-injection scanner, live) and **[guardrail-arena](https://github.com/fevziegeyurtsevenler/guardrail-arena)** (two-axis EN+TR guardrail benchmark; finding: guards over-refuse 40–70% of security-adjacent text, `jackhhao/jailbreak-classifier` misses 83% of Turkish attacks). Full tool index: **[altaysec.com.tr/acik-kaynak](https://altaysec.com.tr/acik-kaynak)**.

---

## 🤝 Katkı

Katkılar memnuniyetle karşılanır. Dahil edilme ölçütü: Türkçe yapay zeka güvenliğiyle ilgili, açık kaynak, bakımı yapılan ve iddiası tekrar üretilebilir çalışmalar. Öneri/düzeltme için Issue açın veya PR gönderin.

---

## 🔗 Bağlantılar

- 🌐 Web: [altaysec.com.tr](https://altaysec.com.tr)
- 🎓 Akademi: [ai.altaysec.com.tr](https://ai.altaysec.com.tr)
- 🧰 Açık kaynak araçlar (23+): [altaysec.com.tr/acik-kaynak](https://altaysec.com.tr/acik-kaynak)
- 🤗 Hugging Face: [huggingface.co/fevziegeyurtsevenler](https://huggingface.co/fevziegeyurtsevenler)
- 💼 LinkedIn: [Fevzi Ege Yurtsevenler](https://www.linkedin.com/in/fevziegeyurtsevenler/)
- 🧾 DOI: [10.5281/zenodo.20681557](https://doi.org/10.5281/zenodo.20681557) · ORCID: [0009-0008-6518-8944](https://orcid.org/0009-0008-6518-8944)

---

<sub>© 2026 AltaySec · Türkçe yapay zeka güvenliği için açık kaynak araçlar ve veri setleri · Kurucu: Fevzi Ege Yurtsevenler · Ankara, Türkiye</sub>

---

## İlgili AltaySec Kaynakları

- 📖 [AI Security Öğrenme Rehberi — Sıfırdan Uzmanlığa](https://altaysec.com.tr/arastirmalar/ai-security-ogrenme-rehberi) — konunun derinlemesine Türkçe analizi
- 🌐 [AltaySec Araştırmalar](https://altaysec.com.tr/arastirmalar/) — Türkçe yapay zekâ güvenliği yazıları
