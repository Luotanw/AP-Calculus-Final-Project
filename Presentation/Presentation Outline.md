# Presentation Outline: Introducing Trig Sub

Goal: Introduce trigonometric substitution through one worked example:

$$
\int \frac{dx}{\sqrt{x^2-1}}
$$

Main message: Trigonometric substitution is useful when a radical contains a quadratic expression that matches a Pythagorean identity.

---

## 1. Opening Problem: Why This Integral Is Difficult (0:00-1:00)

Show the example:

$$
\int \frac{dx}{\sqrt{x^2-1}}
$$

Explain the obstacle:

- The square root makes the integral hard to be handled.
- A normal $u$-substitution does not simplify it cleanly.
- If $u=x^2-1$, then $du=2x\,dx$, but there is no $x$ in the numerator.

Transition:

The expression $x^2-1$ looks similar to the identity

$$
\sec^2\theta-1=\tan^2\theta
$$

so we try to rewrite $x$ as a secant function.

---

## 2. Choosing the Substitution (1:00-2:15)

Since the radical has the form

$$
\sqrt{x^2-1}
$$

use

$$
x=\sec\theta
$$

Then

$$
dx=\sec\theta\tan\theta\,d\theta
$$

Explain why this substitution is chosen:

$$
\sqrt{x^2-1}
=\sqrt{\sec^2\theta-1}
=\sqrt{\tan^2\theta}
=|\tan\theta|
$$

Key point:

The absolute value matters. This is where domain restrictions enter the solution.

---

## 3. Domain and Range Restrictions (2:15-3:30)

The original integrand is only defined when

$$
x^2-1>0
$$

so

$$
x\in(-\infty,-1)\cup(1,\infty)
$$

To make $x=\sec\theta$ reversible, restrict $\theta$ to

$$
\theta\in\left(0,\frac{\pi}{2}\right)\cup
\left(\frac{\pi}{2},\pi\right)
$$

This gives the two branches:

$$
\begin{cases}
x>1, & 0<\theta<\frac{\pi}{2} \\
x<-1, & \frac{\pi}{2}<\theta<\pi
\end{cases}
$$

Important sign fact:

$$
\tan\theta
\begin{cases}
>0, & 0<\theta<\frac{\pi}{2} \\
<0, & \frac{\pi}{2}<\theta<\pi
\end{cases}
$$

This determines how to simplify $|\tan\theta|$.

---

## 4. Substitute Into the Integral (3:30-5:15)

Start with

$$
\int \frac{dx}{\sqrt{x^2-1}}
$$

Substitute $x=\sec\theta$ and $dx=\sec\theta\tan\theta\,d\theta$:

$$
\int
\frac{\sec\theta\tan\theta}{\sqrt{\sec^2\theta-1}}
\,d\theta
$$

Use the identity:

$$
\sqrt{\sec^2\theta-1}
=\sqrt{\tan^2\theta}
=|\tan\theta|
$$

So the integral becomes

$$
\int
\frac{\sec\theta\tan\theta}{|\tan\theta|}
\,d\theta
$$

Split by branch:

$$
\begin{cases}
\displaystyle \int \sec\theta\,d\theta,
& 0<\theta<\frac{\pi}{2} \\[1em]
\displaystyle \int -\sec\theta\,d\theta,
& \frac{\pi}{2}<\theta<\pi
\end{cases}
$$

Presentation note: This is the main "payoff" step. The radical disappears because of the trig identity.

---

## 5. Integrate in Terms of $\theta$ (5:15-6:30)

Use the standard result:

$$
\int \sec\theta\,d\theta
=\ln|\sec\theta+\tan\theta|+C
$$

Therefore,

$$
\begin{cases}
\ln|\sec\theta+\tan\theta|+C_1,
& 0<\theta<\frac{\pi}{2} \\[0.8em]
-\ln|\sec\theta+\tan\theta|+C_2,
& \frac{\pi}{2}<\theta<\pi
\end{cases}
$$

Keep this part brief. The focus of the presentation is the substitution, not proving the integral of secant.

---

## 6. Back-Substitute to Return to $x$ (6:30-8:00)

Since

$$
x=\sec\theta
$$

we need $\tan\theta$ in terms of $x$.

Using

$$
\tan^2\theta=\sec^2\theta-1
$$

gives

$$
\tan\theta
=
\begin{cases}
\sqrt{x^2-1}, & x>1 \\[0.8em]
-\sqrt{x^2-1}, & x<-1
\end{cases}
$$

So the antiderivative is

$$
\int \frac{dx}{\sqrt{x^2-1}}
=
\begin{cases}
\ln\left(x+\sqrt{x^2-1}\right)+C_1,
& x>1 \\[0.8em]
-\ln\left(-x+\sqrt{x^2-1}\right)+C_2,
& x<-1
\end{cases}
$$

Emphasize:

The answer is piecewise because the original function has two separate domain intervals.

---

## 7. Quick Interpretation or Verification (8:00-9:15)

Use one of these, depending on slide time:

Option A: Graphical interpretation

- The integrand is only defined on $x<-1$ and $x>1$.
- It becomes very large near $x=-1$ and $x=1$.
- The antiderivative should have very steep slopes near those points.

Option B: Quick derivative check

State that differentiating the final answer on each branch gives

$$
\frac{1}{\sqrt{x^2-1}}
$$

This confirms the result.

---

## 8. Conclusion: What Trig Substitution Does (9:15-10:00)

Summarize the method:

1. Identify the radical form.
2. Match it to a Pythagorean identity.
3. Choose the trig substitution.
4. Restrict the trig function so the substitution is reversible.
5. Use the identity to remove the radical.
6. Back-substitute carefully, including signs and absolute values.

Final takeaway:

Trigonometric substitution is not just a trick. It works because certain radicals are disguised Pythagorean identities.

