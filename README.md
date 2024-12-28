# Catecismo JSON
O presente repositório contém uma cópia fiel em .json do conteúdo do catecismo disponibilizado gratuitamente no [site do vaticano](https://www.vatican.va/archive/cathechism_po/index_new/prima-pagina-cic_po.html), e foi criado a fim de facilitar a criação de novos sites ou aplicativos que queiram exibir o conteúdo do catecismo.
Cada arquivo json está localizado nas subpastas finais conforme a organização do próprio site do vaticano, mas para facilitar o downlaod dos arquivos também fiz uma pasta que contém todos os arquivos das demais chamada "Todos os arquivos". 

## Objeto json padrão para cada pasta
O padrão de nomenclatura do objeto é sempre o mesmo: "p" + número da parte, "s" + número da seção, "c" + número do capítulo". Exemplo:
```json
{
    "nome": "p2_s2",
    "primeiroParagrafo": 1210,
    "ultimoParagrafo": 1211,
    "conteudo": [
        {
            "tipo": "título",
            "texto": "SEGUNDA PARTE"
        },
        {
            "tipo": "título",
            "texto": "A CELEBRAÇÃO\nDO MISTÉRIO CRISTÃO\n\n"
        },
        {
            "tipo": "título",
            "texto": "SEGUNDA SECÇÃO"
        },
        {
            "tipo": "título",
            "texto": "OS SETE SACRAMENTOS DA IGREJA"
        },
        {
            "tipo": "parágrafo",
            "texto": "1210. Os sacramentos da nova Lei foram instituídos por Cristo e são em número de sete, a saber: o Baptismo, a Confirmação, a Eucaristia, a Penitência, a Unção dos Enfermos, a Ordem e o Matrimónio. Os sete sacramentos tocam todas as etapas e momentos importantes da vida do cristão: outorgam nascimento e crescimento, cura e missão à vida de fé dos cristãos. Há aqui uma certa semelhança entre as etapas da vida natural e as da vida espiritual (1).",
            "paragrafo": 1210
        },
        {
            "tipo": "parágrafo",
            "texto": "1211. Seguindo esta analogia, exporemos primeiro os três sacramentos da iniciação cristã (capítulo primeiro), depois os sacramentos de cura (capítulo segundo) e finalmente os que estão ao serviço da comunhão e da missão dos fiéis (capítulo terceiro). Esta ordem não é, certamente, a única possível, mas permite ver que os sacramentos formam um organismo, no qual cada sacramento particular tem o seu lugar vital. Neste organismo, a Eucaristia ocupa um lugar único, como «sacramento dos sacramentos»: «todos os outros sacramentos estão ordenados para este, como para o seu fim» (2).",
            "paragrafo": 1211
        }
    ],
    "referencias": [
        {
            "tipo": "referência",
            "texto": "1. São Tomás de Aquino, Summa theologiae, 3. q. 65, a. 1. c: Ed. Leon. 12, 56-57."
        },
        {
            "tipo": "referência",
            "texto": "2. São Tomás de Aquino, Summa theologiae, 3. q. 65. a. 3. c: Ed. Leon. 12, 60."
        }
    ]
}
```
O objeto padrão de cada item de texto só possui o atributo "paragrafo" que contém o número quando o atributo "tipo" for igual a "parágrafo", caso contrário é nulo. 

## Tipos de texto
O atríbuto "tipo" de cada item de texto foi feito para diferenciar as formatações presentes no site do vaticano, seguem os diferentes tipos e exemplos de casos onde cada um deles foi utilizado:
- título:
<img src="https://github.com/user-attachments/assets/1f03bf1a-a2aa-4ade-8f03-f9c2df97718a" alt="título">

- subtítulo:
<img src="https://github.com/user-attachments/assets/9e0d91ce-4899-4c35-8b1d-43148bb01bd6" alt="subtítulo">

- tópico:
<img src="https://github.com/user-attachments/assets/bd853725-f159-44da-b25d-fc58b6ba55d4" alt="tópico">

- subtópico:
<img src="https://github.com/user-attachments/assets/12dc5ba3-d069-4757-a20b-d0b74bb22382" alt="subtópico">

- parágrafo:
<img src="https://github.com/user-attachments/assets/44ae7a28-3369-4a8f-af2a-5cd80efe0423" alt="parágrafo">

- referência:
<img src="https://github.com/user-attachments/assets/ec7bb4a2-ae12-42d6-83ae-d70441a956a8" alt="referência">

- texto simples:
<img src="https://github.com/user-attachments/assets/1a5a05a1-31e8-442a-bb37-c9b0a9461c97" alt="texto simples">

- coluna 1, coluna 2, coluna 3:
<img src="https://github.com/user-attachments/assets/d77f5705-0495-4ebc-bbc1-549c2ce75477" alt="coluna 1, coluna 2, coluna 3">
<img src="https://github.com/user-attachments/assets/0226a780-ff05-4ed2-910c-0d122db444a5" alt="coluna 1, coluna 2, coluna 3">

OBS: Os tipos "coluna 1", "coluna 2" e "coluna 3" só aparecem na tabela do credo e dos mandamentos, no caso da tabela dos mandamentos, onde os do Êxodo 20 estão na primeira coluna, cada objeto (mandamento) dessa coluna será um objeto do tipo "coluna 1", funciona da mesma forma para todas as demais tabelas.


