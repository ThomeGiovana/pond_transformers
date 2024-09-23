# pond_transformers
 
Giovana Thomé

Ciência da Coputação 

Módulo 11 - 2024.2

# Arquitetura de um modelo transformer

Um transformer é um tipo de rede neural, porém com arquitetura diferente:
- Entrada: Cada palavra da sequência é convertida em um vetor (embedding), e uma codificação posicional é adicionada para indicar a ordem das palavras.
- Mecanismo de Atenção: O modelo calcula, para cada palavra (query), o quanto deve prestar atenção em todas as outras (keys) e aplica essas informações (values).
- Camadas Feedforward: Após a atenção, passa-se por camadas totalmente conectadas para processamento adicional.
- Saída: O modelo gera previsões ou a próxima palavra da sequência.

# Percepções sobre o modelo 

## Uso de transformers para tradução é bom por conta da codificação posicional

A codificação posicional fixa pode ser desnecessária em algumas situações porque nem sempre a posição exata de uma palavra na frase é importante. O que muitas vezes importa mais é a relação entre as palavras, e a codificação fixa força o modelo a sempre prestar atenção na posição.

Em um modelo de tradução, como o analisado, o uso de codificação posicional pode trazer vantagens justamente pela ordem das palavras ser importante.

