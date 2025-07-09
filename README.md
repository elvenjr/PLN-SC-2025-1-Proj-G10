Classificador , em português-BR, capaz de reconhecer 5 intenções comuns em mensagens de suporte:

| Intenção | Exemplo |
|----------|---------|
| `saudacao` | “Olá, bom dia!” |
| `solicitar_info_produto` | “Quero saber o preço do plano premium” |
| `reclamar_servico` | “Estou há horas sem conseguir acessar minha conta” |
| `agradecer` | “Muito obrigado pela ajuda!” |
| `despedida` | “Até a próxima!” |

O pipeline usa **TF-IDF (1–2 gramas) + Multinomial Naïve Bayes**.  
Acurácia final: **80,95 %**.

---

##  Conteúdo do repositório
| Caminho | Conteúdo | Como obter |
|---------|----------|------------|
| `PLN_S2_Intencoes_ElvenJr.ipynb` | Notebook principal — **gera dataset, script e métricas** | já presente |
| `README.md` | Este guia rápido | manual |


---

##  Como reproduzir

### Google Colab  
1. Abra o notebook (botão **Open in Colab** no topo).  
2. Selecione **Runtime ▸ Run all**.  
3. Ao final, o terminal exibe a tabela de métricas e a acurácia.

### Execução local
```bash
git clone https://github.com/PLN-UFSCar/PLN-SC-2025-1-Proj-G10.git
cd PLN-SC-2025-1-Proj-G10
pip install pandas==2.2.2 scikit-learn==1.5.0 nltk==3.8.1 seaborn==0.13.2 matplotlib==3.9.0
python src/intent_classifier.py   # será gerado pelo notebook ou por você
