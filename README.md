# Projeto de Classificação de Pokémon com Redes Neurais Convolucionais (CNN)

## Descrição
Este projeto foi desenvolvido como trabalho final da disciplina de Inteligência Artificial. O objetivo foi implementar e avaliar uma Rede Neural Convolucional (CNN) para a classificação de imagens de Pokémon.

## 📊 Conjunto de Dados
O dataset utilizado foi o **PokemonData**, contendo imagens de 150 espécies diferentes de Pokémon. As imagens foram:
- Redimensionadas para 120x120 pixels
- Normalizadas com as médias e desvios padrão do ImageNet
- Divididas em:
  - 80% para treino
  - 20% para validação

## 🧠 Metodologia
### Arquitetura da CNN
- **Camadas Convolucionais:** 3 camadas com:
  - 32 filtros, kernel 3x3, padding 1
  - Batch Normalization
  - Função de ativação ReLU
  - MaxPooling 2x2 (stride 2)
- **Camadas Densas:**
  - 256 neurônios com Dropout de 0.5
  - 150 neurônios na saída (1 por classe de Pokémon)

### Hiperparâmetros
| Atributo          | Valor           |
|-------------------|-----------------|
| Tamanho do batch  | 32              |
| Número de épocas  | 20              |
| Taxa de aprendizado | 0.001         |

### Otimizador
- AdamW com taxa de decaimento de 0.00001

### Métricas
- Acurácia
- Função de perda: Entropia cruzada

## 🔬 Resultados
O modelo foi treinado com diferentes hiperparâmetros. O melhor desempenho foi:

| Taxa de Aprendizado | Batch Size | Acurácia (%) |
|--------------------|------------|--------------|
| 0.001              | 64         | **74.63**    |

## 🚀 Como Executar
1. Clone o repositório:
   ```bash
   git clone https://github.com/seu-usuario/pokemon-cnn-classifier.git
   ```
2. Instale as dependências:
   ```bash
   pip install -r requirements.txt
   ```
3. Execute o treinamento:
   ```bash
   python train.py
   ```
