# Digital Leaky Integrator: Terminology and Applications

## The Formula
The digital leaky integrator follows this difference equation:
```
y[n] = α * x[n] + (1 - α) * y[n-1]
```

Where α is the leak factor (0 < α ≤ 1). This is mathematically identical to a first-order IIR low-pass filter.

## When to Call It "Leaky Integrator" vs "Low-Pass Filter"

These terms describe the **same mathematical operation** but emphasize different aspects:

### "Leaky Integrator" Perspective
**Use when thinking about:** Accumulation, building up values over time, tracking, approaching targets

**Mental model:** "I'm adding things up over time, but with natural decay to prevent infinite buildup"

**The 'leak' prevents:** Infinite accumulation, system saturation, runaway values

### "Low-Pass Filter" Perspective  
**Use when thinking about:** Removing unwanted frequencies, smoothing signals, spectral shaping

**Mental model:** "I'm filtering out high-frequency components while preserving low-frequency content"

**The filtering removes:** High-frequency noise, rapid fluctuations, unwanted harmonics

## Application Examples and Reasoning

### Envelope Following → "Leaky Integrator"
**Reasoning:** You're accumulating the signal's energy over time. When audio is loud, the envelope "charges up." During quiet periods, it needs to "discharge" naturally.

**Process:**
1. Rectify the audio signal (get instantaneous energy)
2. **Integrate** this energy over time to build the envelope  
3. **Leak** allows natural decay during quiet passages

**Parameter meaning:** α controls attack/release - how quickly energy accumulates and discharges.

### Portamento/Gliding → "Leaky Integrator"
**Reasoning:** You're smoothly approaching a target value. The system naturally "wants" to reach the target.

**Behavior:** Exponential approach to target - fast movement initially, slowing as you get closer.

**Process:** When target changes, you gradually move toward it rather than jumping instantly.

**Parameter meaning:** α controls glide speed - higher α = faster approach to target.

### Running Averages with Decay → "Leaky Integrator"
**Examples in music:**
- **Tempo tracking:** Recent beat intervals influence BPM estimate more than older ones
- **Pitch tracking:** Recent frequency estimates matter more for auto-tune systems
- **Dynamic range metering:** Recent loudness contributes more to current reading

**Reasoning:** You're computing weighted averages where recent data has exponentially more influence than old data.

**Why not just "cheap filtering":** The exponential weighting is often exactly what you want - it's adaptive and naturally emphasizes recent information.

### General Signal Smoothing → Either Term Works
**"Low-pass filter"** if you're thinking: "Remove jitter/noise from my control signal"

**"Leaky integrator"** if you're thinking: "Gradually track changes in my signal"

## Linear vs Exponential Glide

**Linear glide:** Constant rate of change toward target
```
step_size = (target - current) / glide_time
current[n] = current[n-1] + step_size
```

**Exponential glide (leaky integrator):** Fast initially, slowing as you approach target
```
current[n] = α * target + (1-α) * current[n-1]
```

**Simple integrator:** Just accumulates inputs indefinitely
```
y[n] = y[n-1] + x[n]
```

## Key Insight

The terminology choice reflects your **mental model** of what the system is doing:
- **Time-domain, accumulation-focused thinking** → "leaky integrator"  
- **Frequency-domain, filtering-focused thinking** → "low-pass filter"

Both are correct, but one usually fits the application context better than the other.