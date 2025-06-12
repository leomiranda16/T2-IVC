# Detecção de Sonolência em Motoristas com Visão Computacional

Este projeto tem como objetivo detectar sinais de sonolência em motoristas utilizando técnicas de visão computacional. A aplicação identifica comportamentos como fechamento prolongado dos olhos, frequência de piscadas e expressões faciais (como o riso) para inferir possíveis sinais de cansaço.

O sistema foi implementado em Python utilizando as bibliotecas **OpenCV**, **MediaPipe** e **NumPy**, com interface em um Jupyter Notebook. Este trabalho foi desenvolvido como parte da disciplina **Introdução à Visão Computacional**, no curso de Ciência de Dados e Inteligência Artificial.

## 📁 Conteúdo do Repositório

- `relatorio.pdf` — Artigo técnico explicando o funcionamento do sistema, a base teórica e os resultados obtidos.
- `projeto.ipynb` — Notebook Jupyter com o código-fonte do projeto, incluindo visualizações e comentários explicativos.
- `requirements.txt` — Lista com as bibliotecas necessárias para execução do notebook.
- `README.md` — Este arquivo, com instruções de uso e informações do projeto.
- `apresentação.pptx` — Power Point com os slides apresentados durante a aula de entrega.

## 🧪 Tecnologias Utilizadas

- **Python 3.9.23**
- OpenCV
- MediaPipe
- NumPy
- Jupyter Notebook

## 🚀 Como Executar

Siga os passos abaixo para configurar e executar o projeto em sua máquina local.

1.  **Crie um ambiente virtual (recomendado):**
    ```bash
    python -m venv venv
    ```
    ```bash
    # Para ativar o ambiente virtual
    # No macOS/Linux:
    source venv/bin/activate
    
    # No Windows:
    venv\Scripts\activate
    ```

2.  **Instale as dependências:**
    Certifique-se de que seu ambiente virtual esteja ativado e execute o comando abaixo para instalar as bibliotecas necessárias.
    ```bash
    pip install -r requirements.txt
    ```

3.  **Execute o notebook:**
    Finalmente, inicie o Jupyter Notebook para ver e executar o código principal.
    ```bash
    jupyter notebook codigo.ipynb
    ```

## 🧠 Conceitos Utilizados

O sistema se baseia em métricas faciais calculadas em tempo real a partir do feed de vídeo.

### 👁️ **EAR (Eye Aspect Ratio)**
O EAR (Proporção de Abertura Ocular) é uma métrica crucial para medir o quão abertos ou fechados os olhos estão. Um valor de EAR que permanece abaixo de um limiar pré-definido por um certo número de frames consecutivos é interpretado como um forte sinal de sonolência.

### 😄 **MAR (Mouth Aspect Ratio)**
O MAR detecta o riso, que provoca a abertura da boca e o fechamento dos olhos, o que poderia gerar falsos positivos de sonolência. Ao monitorar o MAR, o sistema pode identificar esses casos e evitar alarmes incorretos.

### 👀 **Detecção de Piscadas**
A frequência de piscadas é monitorada com base nas variações do EAR. Uma taxa de piscadas anormalmente baixa pode ser um indicador de fadiga ou esforço visual, contribuindo para a avaliação geral do estado do usuário.

---

## 👨‍💻 Autores
* **Guilherme Scherer**
* **Leonardo Miranda**

**Disciplina:** Introdução à Visão Computacional  
**Instituição:** Ciência de Dados e Inteligência Artificial – PUCRS  
**Data:** Junho de 2025

## 📜 Licença
Este projeto é destinado a fins educacionais e acadêmicos. Sinta-se à vontade para estudar, modificar e adaptar o código para seus próprios projetos de aprendizado.
