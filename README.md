# 🐜 Cupimatico

Rastreador inteligente para cupins em arenas 2D - Um sistema de análise de comportamento e movimento de cupins em ambientes controlados.

## 📋 Sobre

Cupimatico é uma ferramenta de pesquisa desenvolvida para rastrear e analisar o comportamento de cupins em arenas bidimensionais. O projeto fornece:

- **Rastreamento em Tempo Real**: Monitora a posição e movimento de múltiplos cupins simultaneamente
- **Análise de Padrões**: Identifica padrões de movimento, exploração e comportamento colaborativo
- **Visualização Interativa**: Interface visual para observar e analisar a atividade dos cupins
- **Coleta de Dados**: Registro detalhado de trajetórias para análise posterior

## 🚀 Quick Start

### Pré-requisitos

- Python 3.8+
- pip ou conda
- (Adicione outros requisitos conforme necessário)

### Instalação

```bash
# Clone o repositório
git clone https://github.com/rrgrig/cupimatico.git
cd cupimatico

# Crie um ambiente virtual
python -m venv venv
source venv/bin/activate  # No Windows: venv\Scripts\activate

# Instale as dependências
pip install -r requirements.txt
```

### Uso Básico

```bash
# Inicie o rastreador
python main.py

# Execute a análise de dados
python analyze.py --input data/arena.csv
```

## 📁 Estrutura do Projeto

```
cupimatico/
├── README.md
├── requirements.txt
├── main.py                 # Entrada principal
├── src/
│   ├── tracker.py         # Sistema de rastreamento
│   ├── arena.py           # Definição da arena
│   └── analysis.py        # Análise de padrões
├── data/
│   └── samples/           # Dados de exemplo
├── tests/
│   └── test_tracker.py    # Testes unitários
└── docs/
    └── API.md             # Documentação da API
```

## 🔧 Tecnologias

- **Python 3**: Linguagem principal
- **OpenCV**: Processamento de imagem e visão computacional
- **NumPy/Pandas**: Análise de dados
- **Matplotlib/Plotly**: Visualização
- **pytest**: Testes automatizados

## 📊 Exemplo de Uso

```python
from src.tracker import AntTracker
from src.arena import Arena2D

# Cria arena 100x100 pixels
arena = Arena2D(width=100, height=100)

# Inicializa rastreador
tracker = AntTracker(arena)

# Processa vídeo/imagens
tracker.process_frame(frame)

# Obtém dados rastreados
trajectories = tracker.get_trajectories()
print(f"Cupins detectados: {len(trajectories)}")
```

## 📈 Features Planejadas

- [ ] Integração com câmeras em tempo real
- [ ] Machine learning para classificação de comportamento
- [ ] Exportação de relatórios em PDF
- [ ] Dashboard web interativo
- [ ] Suporte para múltiplas arenas simultâneas
- [ ] API REST para integração externa

## 🤝 Contribuindo

Contribuições são bem-vindas! Por favor:

1. Faça um fork do repositório
2. Crie uma branch para sua feature (`git checkout -b feature/AmazingFeature`)
3. Commit suas mudanças (`git commit -m 'Add some AmazingFeature'`)
4. Push para a branch (`git push origin feature/AmazingFeature`)
5. Abra um Pull Request

## 📝 Licença

Este projeto está sob a licença MIT. Veja o arquivo `LICENSE` para mais detalhes.

## ✉️ Contato

- **Autor**: rrgrig
- **GitHub**: [@rrgrig](https://github.com/rrgrig)
- **Issues**: [Abra uma issue](https://github.com/rrgrig/cupimatico/issues)

## 🔗 Recursos Úteis

- [Documentação Completa](./docs/API.md)
- [Guia de Instalação](./docs/INSTALL.md)
- [Changelog](./CHANGELOG.md)
- [Roadmap](./docs/ROADMAP.md)

---

**Desenvolvido com ❤️ para pesquisa em comportamento de insetos**