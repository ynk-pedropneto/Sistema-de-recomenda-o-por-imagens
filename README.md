# 🔎 Image Similarity Recommender

Este projeto implementa um **Sistema de Recomendação baseado em imagens** usando Deep Learning.
A recomendação é feita por **similaridade visual** (forma, cor, textura), sem depender de metadados como preço ou marca.

## 🚀 Como funciona
1. Extraímos **features visuais** das imagens com uma CNN pré-treinada (**ResNet50**, ImageNet).
2. Calculamos a **similaridade do cosseno** entre os vetores de features.
3. Retornamos as imagens mais parecidas com a imagem de consulta (query).

## 📂 Estrutura
```
image-recommender/
│── data/                # Imagens do dataset (coloque as suas aqui)
│── notebooks/           # Notebook principal
│── src/                 # Código fonte
│   │── feature_extractor.py
│   │── recommender.py
│── requirements.txt     # Dependências
│── README.md            # Documentação
│── .gitignore
```
> Dica: você pode criar subpastas dentro de `data/` conforme categorias (ex: `data/relogios/`, `data/camisetas/`).

## ▶️ Execução
```bash
# 1) Crie e ative um ambiente virtual (opcional, mas recomendado)
python -m venv .venv
# Windows: .venv\Scripts\activate
# macOS/Linux: source .venv/bin/activate

# 2) Instale as dependências
pip install -r requirements.txt

# 3) Rode o notebook
jupyter notebook notebooks/image_recommender.ipynb
```

No notebook você poderá:
- Indexar todas as imagens em `data/`
- Escolher uma imagem de consulta
- Visualizar as **Top-K** imagens mais similares (com as respectivas pontuações)

## 🔄 Trocar o backbone (opcional)
Se preferir uma arquitetura mais leve, substitua `ResNet50` por `MobileNetV2` no `feature_extractor.py`.

## 📘 Licença
Uso acadêmico/educacional. Ajuste conforme sua necessidade.
