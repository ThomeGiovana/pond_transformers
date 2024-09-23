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

## Implementação fiel à arquitetura

Um ponto positivo dessa implementação é que ela segue exatamente a arquitetura padrão de um decoder em um modelo transformer, incluindo componentes essenciais como a atenção multi-cabeças e as camadas de feed-forward. Isso facilita a compreensão do fluxo de dados, ajudando no aprendizado.

## Implementação com erros

Por outro lado, um ponto negativo é que a implementação não inclui tratamento de exceções ou validações adicionais para entradas inesperadas. Por exemplo, se forem fornecidos valores nulos ou formatos de dados incorretos, o código pode não lidar adequadamente com esses casos. Adicionar verificações e tratamentos de erro poderia tornar a implementação mais robusta e confiável em diferentes cenários.

Por exemplo, na implementação das camadas de codificação e decodificação, foram encontrados erros por conta da tipagem dos parâmetros passados para os métodos das classes.

