```mermaid
sequenceDiagram
    participant ESP32
    participant Backend
    participant Frontend

    ESP32->>Backend: Envia dados de temperatura e umidade em formato JSON
    Backend->>ESP32: Confirma recebimento dos dados
    Frontend->>Backend: Faz requisições HTTP para obter dados em tempo real
    Backend->>Frontend: Retorna dados processados para exibição
    Frontend->>Backend: Envia comandos de controle (ex.: ajustar temperatura ou ativar irrigação)
    Backend->>ESP32: Envia comandos para os atuadores (lâmpada, bomba)
    ESP32->>Backend: Confirma execução dos comandos
    Backend->>Frontend: Atualiza status do sistema

    
