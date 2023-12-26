---
title: Proof of Parseval's theorem
author: Haru
date: 2023-12-26 11:33:00 +0800
categories: [Blogging]
tags: [math]
pin: true
math: true
mermaid: true
---

Let $f(t)$ be a function with Fourier transform $F(\omega)$. Then, Parseval's Theorem states that

$$
\int_{-\infty}^{\infty} |f(t)|^2 \, dt = \frac{1}{2\pi} \int_{-\infty}^{\infty} |F(\omega)|^2 \, d\omega
$$

**Proof**

Start with the definition of the Fourier transform:

$$
F(\omega) = \int_{-\infty}^{\infty} f(t) e^{-i\omega t} \, dt
$$

Now, consider the product \(f(t) \cdot \overline{f(t)}\), where \(\overline{f(t)}\) is the complex conjugate of \(f(t)\):

$$
f(t) \cdot \overline{f(t)} = |f(t)|^2
$$

Take the Fourier transform of $f(t) \cdot \overline{f(t)}$:

$$
\mathcal{F}\{f(t) \cdot \overline{f(t)}\} = \int_{-\infty}^{\infty} f(t) \cdot \overline{f(t)} \cdot e^{-i\omega t} \, dt
$$

Since the product is real, \(\overline{f(t)}\) is the complex conjugate of \(f(t)\), and the Fourier transform of a real function is Hermitian, we have:

$$
\mathcal{F}\{f(t) \cdot \overline{f(t)}\} = \int_{-\infty}^{\infty} |F(\omega)|^2 \, d\omega
$$

Now, use the convolution theorem, which states that the Fourier transform of the convolution of two functions is the product of their Fourier transforms:

$$
\mathcal{F}\{f \cdot \overline{f}\} = \frac{1}{2\pi} \mathcal{F}\{f\} * \mathcal{F}\{\overline{f}\}
$$

Substitute the expressions for $\mathcal{F}\{f \cdot \overline{f}\}$ and $\mathcal{F}\{f\}$ into the equation:

$$
\int_{-\infty}^{\infty} |f(t)|^2 \, dt = \frac{1}{2\pi} \int_{-\infty}^{\infty} |F(\omega)|^2 \, d\omega
$$

This completes the proof of Parseval's Theorem.