# 🏰 GALAHAD Timeline - Analisador de WhatsApp

> **Uma ferramenta poderosa para analisar e visualizar suas conversas do WhatsApp em uma timeline unificada com calendário interativo.**

## 📋 Características

- ✅ **Processamento completo** de exportações do WhatsApp
- 📅 **Calendário visual** com intensidade de atividade por dia
- 👥 **Indexação de participantes** e estatísticas detalhadas
- 🖼️ **Suporte a mídia** (fotos, vídeos, áudio, documentos)
- 📊 **Relatórios estatísticos** completos
- 🎨 **Interface HTML** responsiva e elegante
- 🔍 **Busca e filtros** por período, participante e tipo de conteúdo

## 🚀 Instalação Rápida

### Pré-requisitos
- Python 3.8 ou superior
- Sistema operacional: Windows, macOS ou Linux

### Instalação Automática
```bash
# 1. Baixe todos os arquivos do GALAHAD
# 2. Execute o instalador automático
python install.py
```

### Instalação Manual
```bash
# 1. Instalar dependências
pip install -r requirements.txt

# 2. Criar diretórios necessários
mkdir data output
```

## 📁 Estrutura de Pastas

```
galahad_timeline/
├── processar_timeline_unica.py  # Script principal
├── install.py                   # Instalador automático
├── requirements.txt             # Dependências
├── README.md                    # Este arquivo
├── data/                        # Coloque seus chats aqui
│   ├── chat_amigo1/
│   │   ├── _chat.txt           # Arquivo de conversa
│   │   └── [arquivos de mídia] # Fotos, vídeos, etc.
│   └── chat_grupo_familia/
│       ├── _chat.txt
│       └── [arquivos de mídia]
└── output/                      # Resultados gerados
    └── timeline_galahad.html    # Timeline final
```

## 📱 Como Exportar Chats do WhatsApp

### Android:
1. Abra o WhatsApp
2. Vá para o chat desejado
3. Toque nos 3 pontos (⋮) → **Mais** → **Exportar conversa**
4. Escolha **"Incluir mídia"** (recomendado)
5. Salve o arquivo ZIP

### iPhone:
1. Abra o WhatsApp
2. Vá para o chat desejado
3. Toque no nome do contato/grupo no topo
4. Role para baixo → **Exportar Conversa**
5. Escolha **"Anexar Mídia"** (recomendado)
6. Salve o arquivo

### Organização dos Arquivos:
1. **Extraia** cada ZIP exportado
2. **Renomeie** o arquivo `.txt` para `_chat.txt`
3. **Coloque** cada chat em uma pasta separada dentro de `data/`

Exemplo:
```
data/
├── chat_joao/
│   ├── _chat.txt               # Renomeie de "Conversa do WhatsApp com João.txt"
│   ├── IMG-20230115-WA0001.jpg
│   └── VID-20230115-WA0002.mp4
└── chat_familia/
    ├── _chat.txt               # Renomeie de "Conversa do WhatsApp com Família.txt"
    └── [outros arquivos...]
```

## 🎯 Como Usar

### Uso Básico:
```bash
# Execute o processamento
python processar_timeline_unica.py

# Abra o resultado no navegador
open output/timeline_galahad.html  # macOS
start output/timeline_galahad.html # Windows
xdg-open output/timeline_galahad.html # Linux
```

### O que o script faz:
1. 🔍 **Escaneia** a pasta `data/` procurando chats
2. 📖 **Analisa** cada arquivo `_chat.txt`
3. 🖼️ **Indexa** todos os arquivos de mídia
4. 📅 **Gera** calendário com intensidade de atividade
5. 🏗️ **Cria** timeline HTML unificada
6. 📊 **Calcula** estatísticas detalhadas

## 📊 O que você verá no resultado:

### Calendário de Atividade:
- **Visualização anual** com intensidade de cores
- **Hover** mostra estatísticas do dia
- **Cliques** filtram eventos do período

### Timeline de Eventos:
- **Cronologia completa** de todas as conversas
- **Filtros** por pessoa, período e tipo
- **Links clicáveis** em URLs compartilhadas
- **Prévia de mídia** para fotos e vídeos

### Estatísticas:
- 📈 **Total de eventos** processados
- 👥 **Número de participantes**
- 📅 **Período coberto** (datas início/fim)
- 💬 **Distribuição** de tipos de mensagem

## 🛠️ Solução de Problemas

### Erro: "Arquivo não encontrado"
- ✅ Verifique se os arquivos estão em `data/`
- ✅ Certifique-se que o arquivo se chama `_chat.txt`
- ✅ Confirme que a pasta não está vazia

### Erro: "Dependência não encontrada"
```bash
# Reinstale as dependências
pip install --upgrade -r requirements.txt
```

### Performance lenta:
- 💡 **Limite** o número de chats processados
- 💡 **Remova** arquivos de mídia muito grandes
- 💡 **Execute** em máquina com mais RAM

### Problemas de encoding:
- 💡 Certifique-se que os arquivos estão em **UTF-8**
- 💡 No Windows, use o **Bloco de Notas** para salvar em UTF-8

## 🔧 Dependências Opcionais

Para análise completa de mídia, instale:
```bash
pip install mutagen Pillow opencv-python
```

- **mutagen**: Metadados de arquivos de áudio
- **Pillow**: Processamento avançado de imagens
- **opencv-python**: Análise de vídeos

## 📋 Requisitos de Sistema

- **Python**: 3.8+
- **RAM**: 2GB+ (recomendado 4GB+)
- **Disco**: 1GB+ livre
- **CPU**: Qualquer processador moderno

## 📧 Suporte

Para problemas ou dúvidas:
1. Verifique se seguiu todas as instruções
2. Confirme que os arquivos estão organizados corretamente
3. Execute `python install.py` novamente se necessário

## 🎨 Personalização

O arquivo HTML gerado pode ser customizado editando as seções CSS no script `processar_timeline_unica.py`.

---

**Desenvolvido com ❤️ para análise de dados pessoais WhatsApp**
