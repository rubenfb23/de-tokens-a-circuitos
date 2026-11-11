# De tokens a circuitos

Materiales del taller *From Tokens to Circuits*: una introducción a cómo funciona un transformer por dentro y a las herramientas básicas de la interpretabilidad mecanicista.

Impartido en el **DevFest 2026 Ourense** ([GDG Ourense](https://gdgourense.es)), el 7 de noviembre de 2026, en la ESEI (Ourense).

Vídeo: próximamente

## Contenido

### Notebooks

| Archivo | Qué cubre |
|---|---|
| [notebooks/01_de_tokens_a_un_gpt.ipynb](notebooks/01_de_tokens_a_un_gpt.ipynb) | Parte 1. De los tokens a un GPT: tokenización BPE, embeddings, atención (query, key y value, máscara causal y *multi-head*), la arquitectura completa y un preentrenamiento corto con Shakespeare. |
| [notebooks/02_dentro_del_modelo.ipynb](notebooks/02_dentro_del_modelo.ipynb) | Parte 2. Interpretabilidad mecanicista en GPT-2 small con TransformerLens: caché de activaciones, logit lens, *induction heads*, ablación, *activation patching* (tarea IOI) y *steering*. |

[![Abrir la parte 1 en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/rubenfb23/de-tokens-a-circuitos/blob/main/notebooks/01_de_tokens_a_un_gpt.ipynb)
[![Abrir la parte 2 en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/rubenfb23/de-tokens-a-circuitos/blob/main/notebooks/02_dentro_del_modelo.ipynb)

### Diapositivas

| Archivo | Qué cubre |
|---|---|
| [slides/01_from_tokens_to_circuits.pdf](slides/01_from_tokens_to_circuits.pdf) | Parte 1 (18 diapositivas). El mapa del taller, tokenización, atención y la arquitectura GPT. |
| [slides/02_dentro_del_modelo.pdf](slides/02_dentro_del_modelo.pdf) | Parte 2 (16 diapositivas). Residual stream, superposición y las herramientas, de observar a intervenir. |

Las diapositivas van en 16:9. El código de los notebooks está bajo licencia MIT; las diapositivas, bajo [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).

## Cómo ejecutarlo

Los notebooks se publican sin celdas ejecutadas. Al correrlos aparecen las figuras y las animaciones de las diapositivas (celdas `anim(...)`).

### En Colab

Usa los botones de arriba. En la parte 1 conviene una GPU T4: *Entorno de ejecución → Cambiar tipo de entorno de ejecución → GPU*. En CPU también funciona, solo que entrena menos pasos. La parte 2 va más fluida con GPU, pero se puede seguir en CPU.

### En local

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
jupyter notebook notebooks/01_de_tokens_a_un_gpt.ipynb
```

La parte 1 descarga sola el corpus Tiny Shakespeare. La parte 2 descarga GPT-2 small a través de TransformerLens (Hugging Face).

## Recursos

- [Neuronpedia](https://www.neuronpedia.org), para explorar features de *sparse autoencoders* en el navegador
- Anthropic, [Eval awareness in Claude Opus 4.6's BrowseComp performance](https://www.anthropic.com/research/eval-awareness-browsecomp)
- [TransformerLens](https://github.com/TransformerLensOrg/TransformerLens), la librería que usamos en la parte 2
- [ARENA](https://arena.education), curso abierto de interpretabilidad
- [Transformer Circuits](https://transformer-circuits.pub)
- Sebastian Raschka, *Build a Large Language Model (From Scratch)* (el esquema de las tres etapas y el hilo de la parte 1)
- Papers que salen en las diapositivas: Elhage et al. (2021, 2022), Olsson et al. (2022), Wang et al. (2022) y Turner et al. (2023)

## Autor

Ruben Fernandez Boullon — PhD student in mechanistic interpretability of LLMs, lead of GDG Ourense

- [GitHub](https://github.com/rubenfb23)
- [X](https://x.com/rubenfb_23)
- [YouTube](https://www.youtube.com/@rubenfbyt)

---

## English

Notebooks and slides from the workshop *From Tokens to Circuits*, an introduction to how a transformer works and to the basic tools of mechanistic interpretability. Given at DevFest 2026 Ourense (GDG Ourense, ESEI, 7 November 2026).

Part 1 builds a small GPT from tokens, BPE, embeddings and attention, and pretrains it briefly on Shakespeare. Part 2 opens GPT-2 small with TransformerLens and walks through logit lens, induction heads, ablation, activation patching and steering.

Video: coming soon. Code is MIT; slides are CC BY 4.0.
