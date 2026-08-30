# Metodos-Numericos

Simulação de Consumo de Ar Condicionado em Sala Comercial

-Este projeto foi desenvolvido como um trabalho da disciplina de Métodos Numéricos. O objetivo é calcular o custo anual de energia elétrica necessária para climatizar uma sala comercial com ar-condicionado, com base em dados reais de temperatura e parâmetros do ambiente.


O que o código faz?

-Carrega dados de temperatura de um arquivo CSV com temperaturas mínimas e máximas diárias ao longo de um ano.
-Ajusta um modelo anual periódico para as temperaturas usando funções seno e cosseno.
-Define dias úteis (segunda a sexta) e verifica se a temperatura interna ultrapassa 25°C, indicando a necessidade de ligar o ar-condicionado.
-Cria splines cúbicas periódicas para simular a variação da temperatura ao longo do dia, com base em dados de verão e inverno.
-Calcula a energia consumida pelo ar-condicionado em dias úteis, das 8h às 18h.
-Aplica integração numérica usando dois métodos:
-Regra do retângulo (2D)
-Gauss-Legendre (mais preciso)
-Compara os métodos e apresenta o custo final estimado em reais.


Tecnologias utilizadas

-Python 
-Bibliotecas: numpy, pandas, matplotlib, scipy.interpolate e math


Estrutura do código
-Etapa	Descrição
1	Carregamento e análise inicial dos dados de temperatura
2	Ajuste de modelo anual senoidal para Tmin e Tmax
3	Criação de splines cúbicas para temperatura ao longo do dia
4	Modelagem da temperatura externa combinando dados anuais e diários
5	Cálculo da energia com regra do retângulo (2D)
6	Cálculo da energia com Gauss-Legendre e análise de convergência

Resultados obtidos
-Percentual de dias com ar-condicionado ligado: ~90,4%
-Energia consumida anual: ~90.045 kWh
-Custo anual estimado: 68.434,20 reais


Como executar
-Certifique-se de ter o arquivo Dados simplificado - Temp. bulbo seco Min, Med, Max diarios.csv na pasta correta.
-Execute o notebook .ipynb célula por célula, ou converta para script .py.
-As visualizações serão exibidas automaticamente (gráficos e tabelas).

Observações finais

-Os cálculos consideram dias úteis e horário comercial (8h às 18h).
-O modelo utiliza interpolação e integração numérica, garantindo precisão sem a necessidade de dados horários completos.
-O código é didático e pode ser adaptado para outros cenários de climatização ou eficiência energética.
-Se tiver dúvidas ou quiser adaptar para outro contexto, fique à vontade para modificar os parâmetros como F_ger, heff_Atot, T_conforto e a tarifa C.

