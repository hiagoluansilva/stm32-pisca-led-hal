# stm32-pisca-led-hal

Pisca-pisca de LED com velocidade variável usando STM32 HAL e timer TIM10.

## Descrição

Projeto básico gerado pelo STM32CubeMX que demonstra o controle de um LED via HAL com velocidade ajustável. Utiliza o TIM10 como base de tempo e USART2 para comunicação serial de debug.

## Hardware

- Placa: STM32 Nucleo
- LED: PA5 (LED onboard)

## Variável de controle

```c
uint8_t velocidade;  // Controla a frequência do pisca
```

## Periféricos

| Periférico | Função |
|------------|--------|
| TIM10 | Base de tempo do pisca |
| USART2 | Serial debug (115200 bps) |
| GPIO | LED PA5 |

## Como usar

1. Abra no STM32CubeIDE ou Atollic TrueSTUDIO
2. Compile e grave via ST-Link
3. Ajuste o valor de `velocidade` para alterar a frequência

## IDE

Atollic TrueSTUDIO 9.3 / STM32CubeIDE

## Escola

Centro Tecnológico Liberato — Novo Hamburgo/RS
