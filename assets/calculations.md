Amostra de cálculos relacionados à laminação Sendzimir

1) Estimativa simples de deflexão do work roll (modelo simplificado)

- Modelo: rolo de trabalho como viga apoiada com força de contato linear p (N/m).
- Fórmula aproximada (para viga de comprimento L com carga uniformemente distribuída w):
  deflexao_max = 5 w L^4 / (384 E I)

Exemplo numérico (ordens de grandeza):
- Comprimento efetivo de contato L = 0.4 m
- Força por unidade de comprimento w = 1e5 N/m (exemplo)
- Work roll: diâmetro d = 0.05 m, raio r = 0.025 m
- Momento de inércia I (seção circular, eixo neutro): I = (pi/64) d^4 = (pi/64) * (0.05)^4 = 3.07e-9 m^4
- Módulo de elasticidade E ~ 210 GPa = 2.1e11 N/m^2

Calculo:
- deflexao_max ≈ 5 * 1e5 * (0.4^4) / (384 * 2.1e11 * 3.07e-9)
- Numerador = 5 * 1e5 * 0.0256 = 12800
- Denominador = 384 * 2.1e11 * 3.07e-9 ≈ 384 * 644.7 ≈ 247,564
- deflexao_max ≈ 12800 / 247,564 ≈ 0.0517 m (51 mm) -> valor irrealista indicando que a suposição de carga linear w exagerada ou modelo inadequado

Observação: o cálculo acima é apenas ilustrativo para mostrar sensibilidade; na prática, a carga e rígidez são distribuídas de forma complexa e o suporte por backup rolls reduz drasticamente a deflexão. Engenharia detalhada requer modelagem FEM e dados de carga reais.

2) Exemplo de planejamento de passes (simplificado)

- Objetivo: reduzir espessura inicial de 1.00 mm para 0.20 mm em laminador Sendzimir.
- Estratégia: múltiplas passadas com redução moderada por passada (ex.: 25% por passada)

Passos:
- h0 = 1.00 mm
- h1 = h0 * (1 - 0.25) = 0.75 mm
- h2 = 0.75 * 0.75 = 0.5625 mm
- h3 = 0.5625 * 0.75 = 0.4219 mm
- h4 = 0.4219 * 0.75 = 0.3164 mm
- h5 = 0.3164 * 0.75 = 0.2373 mm
- h6 = 0.2373 * 0.75 = 0.1780 mm (abaixo do alvo; ajustar para precisão)

Resultado: com 6 passadas a 25% (redução relativa) alcança-se aproximadamente 0.18 mm. Na prática, ajustes finos são feitos nas últimas passadas.

3) Cálculo simples de tensão na tira (tensão média aproximada)

- Tensão σ = F / A
- Para uma tira 200 mm de largura e 0.5 mm de espessura, área A = 0.2 * 0.0005 = 1e-4 m^2
- Se a força total na seção for 10 kN (10,000 N), σ = 10,000 / 1e-4 = 1e8 Pa = 100 MPa

Observação final: use sempre modelagem detalhada (FEM) e dados reais de processo para dimensionamento; esses exemplos servem apenas para ensino e análise qualitativa.
