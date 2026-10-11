# Data Flow Diagram CyberShield

## DFD Awal

```mermaid
flowchart LR
    U[External Entity: Pengguna]

    P1[Process: Input & Validasi URL]
    P2[Process: Analisis Risiko URL]
    P3[Process: Generate Hasil Analisis]

    D1[(Data Store: Aturan Deteksi)]
    D2[(Data Store: Mock/Sample URL)]

    U -->|URL yang akan dianalisis| P1
    P1 -->|URL valid| P2
    P1 -->|Pesan validasi| U

    D1 -->|Aturan HTTPS, TLD, keyword, extension| P2
    D2 -->|Contoh URL| P1

    P2 -->|Indikator risiko & risk score| P3
    P3 -->|Hasil analisis & rekomendasi| U