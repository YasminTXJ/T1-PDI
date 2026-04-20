
# Segmentação de Objetos em Imagens de Raio-X (Aeroporto)

Este repositório contém a implementação do **Trabalho T1** da disciplina de **Processamento Digital de Imagens (PDI)**. O objetivo principal é a detecção e extração de objetos individuais a partir de uma imagem panorâmica de Raio-X de bagagens, construída por sobreposição.

## 📋 Descrição do Problema

O desafio consiste em processar uma imagem panorâmica onde diversos objetos estão dispostos horizontalmente. O algoritmo deve ser capaz de identificar as fronteiras de cada objeto e salvá-los como arquivos independentes no formato `.png`.

### Premissas:

  * Não existem objetos alinhados verticalmente (apenas horizontalmente).
  * A extração deve ser precisa, isolando o objeto do fundo.
  * **Restrição:** Não é permitido o uso de soluções prontas (frameworks de segmentação "black-box"). O algoritmo deve ser desenvolvido utilizando técnicas fundamentais de PDI.

## 🚀 Tecnologias Utilizadas

  * **Python 3.x**
  * **OpenCV:** Para manipulação e processamento de imagem.
  * **NumPy:** Para operações matriciais.
  * **Matplotlib:** Para visualização dos resultados.

## ⚙️ Fluxo de Processamento

Para alcançar a segmentação, o projeto segue as seguintes etapas:

1.  **Pré-processamento:** Conversão para escala de cinza e aplicação de filtros (como o Gaussiano ou Mediana) para redução de ruído.
2.  **Limiarização (Thresholding):** Aplicação de técnicas de binarização (como Otsu ou adaptativa) para separar o objeto (foreground) do fundo (background).
3.  **Operações Morfológicas:** Uso de operações como *Erosão*, *Dilação* e *Fechamento* para remover pequenos ruídos e preencher buracos dentro dos objetos.
4.  **Detecção de Componentes Conectados:** Identificação de regiões isoladas na imagem binária.
5.  **Extração e Salvamento:** Criação de caixas delimitadoras (*Bounding Boxes*) para cada objeto detectado e exportação da região recortada em formato PNG.

## 📁 Estrutura do Projeto

```text
├── src/
│   └── main.py          # Script principal com a lógica de segmentação
├── images/
│   ├── input/           # Imagem panorâmica original
│   └── output/          # Objetos extraídos em PNG
├── requirements.txt     # Dependências do projeto
└── README.md
```

## 🛠️ Como Executar

1.  **Clone o repositório:**

    ```bash
    git clone https://github.com/YasminTXJ/T1-PDI.git
    cd T1-PDI
    ```

2.  **Instale as dependências:**

    ```bash
    pip install -r requirements.txt
    ```

3.  **Execute o script:**

    ```bash
    python src/main.py
    ```

## 📊 Resultados

Os objetos detectados são salvos automaticamente na pasta `images/output/`. O algoritmo garante que cada item seja isolado respeitando a premissa de disposição horizontal informada no enunciado.

-----

**Autora:** [Yasmin](https://www.google.com/search?q=https://github.com/YasminTXJ)
**Data:** Setembro de 2024

