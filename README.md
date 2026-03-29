# STM32 Pisca LED HAL — Blink com Timer HAL

🇧🇷 **Português** | 🇺🇸 [English](#english)

---

## Português

Exemplo de pisca-pisca (blink) em STM32F4xx usando HAL e TIM10 configurado para 1 Hz, com variável de velocidade.

### O que faz
- Configura **TIM10** via HAL para gerar interrupção a **~1 Hz**
- Variável `velocidade` permite ajustar a frequência de pisca em tempo de execução
- LED alterna no callback de interrupção do timer

### Configuração do Timer (tim.c)
```c
htim10.Init.Prescaler = 8399;   // PSC = 8399
htim10.Init.Period    = 9999;   // ARR = 9999
// Frequência = 84 MHz / (8400 × 10000) = 1 Hz
```

### Variável de controle
```c
uint32_t velocidade;  // multiplica o período base
```

### Estrutura do projeto
- Gerado com **STM32CubeMX**
- Compilado no **Atollic TrueSTUDIO**
- Usa **STM32 HAL** (Hardware Abstraction Layer)

---

## English

LED blink example on STM32F4xx using HAL and TIM10 configured for 1 Hz, with a speed variable.

### What it does
- Configures **TIM10** via HAL to generate interrupts at **~1 Hz**
- Variable `velocidade` allows adjusting blink frequency at runtime
- LED toggles in the timer interrupt callback

### Timer configuration (tim.c)
```c
htim10.Init.Prescaler = 8399;   // PSC = 8399
htim10.Init.Period    = 9999;   // ARR = 9999
// Frequency = 84 MHz / (8400 × 10000) = 1 Hz
```

### Control variable
```c
uint32_t velocidade;  // multiplies the base period
```

### Project structure
- Generated with **STM32CubeMX**
- Built with **Atollic TrueSTUDIO**
- Uses **STM32 HAL** (Hardware Abstraction Layer)
