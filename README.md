# PLN-SC-2025-1 · Projeto G10  
**Classificação de Intenções em Atendimento ao Cliente**  
Seminário 2 — Processamento de Linguagem Natural (PLN) · UFSCar

---

## 📌 Descrição da tarefa
Treinar um classificador que reconheça **5 intenções** em mensagens de suporte em português-BR:

| Intenção                 | Exemplo                                          |
|--------------------------|--------------------------------------------------|
| `saudacao`               | “Olá, bom dia!”                                  |
| `solicitar_info_produto` | “Quero saber o preço do plano premium”           |
| `reclamar_servico`       | “Estou há horas sem conseguir acessar minha conta”|
| `agradecer`              | “Muito obrigado pela ajuda!”                     |
| `despedida`              | “Até a próxima!”                                 |

Pipeline: **TF-IDF (1–2-gramas) + Multinomial Naïve Bayes**  
Acurácia final: **80,95 %**.

---

## 📂 Conteúdo
| Caminho                           | O que é                          |
|-----------------------------------|----------------------------------|
| `PLN_S2_Intencoes_ElvenJr.ipynb`  | Notebook principal — gera dataset, script e métricas |
| `README.md`                       | Este guia                        |

> O notebook cria on-the-fly:  
> `dataset/intent_dataset.csv`, `src/intent_classifier.py` e `results/metrics.json`.

---

## 🚀 Como reproduzir

### Google Colab
1. Clique em **Open in Colab** no topo do notebook.  
2. Selecione **Runtime ▸ Run all** e aguarde.

### Execução local
```bash
git clone https://github.com/elvenjr/PLN-SC-2025-1-Proj-G10.git
cd PLN-SC-2025-1-Proj-G10
pip install pandas==2.2.2 scikit-learn==1.5.0 nltk==3.8.1 seaborn==0.13.2 matplotlib==3.9.0
python src/intent_classifier.py   # arquivo é gerado pelo notebook
