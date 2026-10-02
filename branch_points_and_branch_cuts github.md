# Branch Points and Branch Cuts

Module 1 (Complex Analysis). Notes are based on the lecture notes (pp. 104–122) and Balakrishnan, *Mathematical Physics: Applications and Problems*, Ch. 26 (§26.1–26.2). Page numbers are the printed ones, not PDF pages.

---

> ✍️ **Added by:** <your name(s)>, 2 Oct 2026

### Multivalued functions, branch points and branch cuts (the $z^{1/2}$ example)

**Statement:**
A function such as $f(z)=z^{1/2}$ gives two outputs for each input $z$, so it is multivalued. Each output is a *branch* ($+\sqrt z$ and $-\sqrt z$). The two branches are glued together along a slit running from $z=0$ to $z=\infty$, which is the **branch cut**. The points $z=0$ and $z=\infty$ are the **branch points**. The two copies of the plane, called Riemann sheets, make up the Riemann surface of $z^{1/2}$. On this surface the function is single valued.

Across the cut the function jumps by

$$\operatorname{disc} f(z)\big|_{x>0} = \lim_{\epsilon\to0}\big[f_I(x+i\epsilon)-f_I(x-i\epsilon)\big] = 2\sqrt{x}.$$

**Derivation / justification (condensed):**
Write $z=re^{i\theta}$. For $0<\theta<2\pi$, $f=\sqrt r\,e^{i\theta/2}$, which covers only the upper half of the $w$-plane. To cover the whole $w$-plane, $\theta$ has to run over $[0,4\pi)$. For $2\pi<\theta<4\pi$ we get $f=-\sqrt z$, the second branch.

Call the two branches $f_I=\sqrt z$ and $f_{II}=-\sqrt z$. We pass from sheet I to sheet II by going once around the origin. A second trip around the origin brings us back to sheet I. At $z=0$ and $z=\infty$ we have $f_I=f_{II}$, so the sheets meet there.

By continuity, $\lim f_I(x-i\epsilon)=\lim f_{II}(x+i\epsilon)$ for $x>0$. So

$$\operatorname{disc} f=f_I(x+i\epsilon)-f_{II}(x+i\epsilon)=\sqrt x-(-\sqrt x)=2\sqrt x.$$

The cut does not have to be the positive real axis. It can be any curve from $0$ to $\infty$. What matters is that we specify the phase of $f$ just above and just below the cut. The choice of cut also fixes the range of the argument.

**Worked example:**
Take the cut along the positive real axis and the principal sheet $0<\theta<2\pi$.

- Just above the cut, $\arg\sqrt z = 0$.
- Just below the cut, $\arg\sqrt z = \pi$.
- On the negative real axis, $\arg\sqrt z=\pi/2$.

Now check whether $z=2$ is a branch point. Go round the circle $|z-2|=1$, which does not enclose $0$. The argument $\theta$ of $z$ goes up to a maximum and comes back down, with no net winding of $2\pi$. So $f(z)$ returns to its starting value and $z=2$ is **not** a branch point. By contrast, going once around the unit circle sends $f\to -f$, so $z=0$ is one.

**Pitfalls / conditions to watch:**
- A closed loop that encircles exactly one branch point is not really closed. We end up on a different sheet.
- No function can have just one branch point. The minimum is two, and a cut joins them. For $z^{1/2}$ the second one sits at $\infty$.
- Always say which sheet you are on and which phase convention you are using before computing a discontinuity.
- Exercise left in the notes: find the discontinuity across the positive imaginary axis when the cut is taken there instead.

---

> ✍️ **Added by:** <your name(s)>, 2 Oct 2026

### Types of branch points: algebraic, winding and logarithmic

**Statement:**

| Type | Example | Branch points | Number of sheets |
|---|---|---|---|
| Algebraic | $z^{p/q}$ ($p,q$ coprime integers, $q>0$) | $0,\infty$ | $q$ |
| Winding | $z^{\alpha}$, $\alpha$ irrational | $0,\infty$ | infinite |
| Logarithmic | $\ln z$ | $0,\infty$ | infinite |

For $z^{p/q}$, the phase jump across the cut is $2\pi p/q$. After $q$ turns around the origin the function returns to its starting value. A plain power $z^p$ with $p$ an integer has no branch point.

**Derivation / justification (condensed):**
For $z^{1/3}$, going once around $z=0$ multiplies the function by $e^{2\pi i/3}$, so three turns are needed to close up. We therefore need three copies of the $z$-plane to cover the $w$-plane once. The sheets are labelled I, II and III. Crossing the cut takes you down one sheet, and crossing it on the lowest sheet takes you back to the top.

For $z^\alpha$ with $\alpha$ irrational, each turn multiplies the function by $e^{2\pi i\alpha}$. Since $e^{2\pi i\alpha n}\neq1$ for every nonzero integer $n$, we can never wind back up to the top sheet. The sheets are labelled by $n\in\mathbb Z$, with the phase of $z$ in $2\pi n<\theta<2\pi(n+1)$. The principal sheet is $n=0$.

For the logarithm, on the $n$th sheet

$$\ln z=\ln r+i\theta+2\pi n i,\qquad n\in\mathbb Z,\ 0\le\theta<2\pi.$$

**Worked example:**
Take $f(z)=z^{-1}\ln(1-z)$. It has logarithmic branch points at $z=1$ and $z=\infty$.

On the principal sheet, $\ln(1-z)\approx -z$ near $z=0$. The simple zero of the log cancels the simple pole of $z^{-1}$, so $z=0$ is only a removable singularity.

On every other sheet, $\ln 1 = 2\pi n i\neq 0$. So $f$ has a genuine **simple pole** at $z=0$ on each of those sheets.

**Pitfalls / conditions to watch:**
- $\ln 1=0$ only on the principal sheet. On the $n$th sheet it is $2\pi n i$.
- Algebraic means finitely many sheets. Winding and logarithmic mean infinitely many.
- The same point $z=0$ can be a regular point on one sheet and a pole on another. Say which sheet you mean when you talk about singularities of multivalued functions.

---

> ✍️ **Added by:** <your name(s)>, 2 Oct 2026

### Finite branch cuts: $(z-a)^{1/2}(z-b)^{1/2}$ and the ratio $\big(\tfrac{z-a}{z-b}\big)^{\alpha}$

**Statement:**
Take $b>a$ real.

- $f(z)=(z-a)^{1/2}(z-b)^{1/2}$ has algebraic branch points at $z=a$ and $z=b$. It is regular at $\infty$, where $f\sim z$. So the cut can be taken as the finite segment from $a$ to $b$.
- The same holds for $\big(\frac{z-a}{z-b}\big)^{1/2}$.
- For any non-integer $\alpha$ (complex included), the ratio $\big(\frac{z-a}{z-b}\big)^{\alpha}$ again has a finite cut from $a$ to $b$.
- The product $(z-a)^{\alpha}(z-b)^{\alpha}$ for $\alpha\neq\tfrac12$ (and not an integer) has **three** branch points, $a$, $b$ and $\infty$. Its cut has to run out to infinity.

**Derivation / justification (condensed):**
Look at each factor separately. For $(z-a)^{1/2}$ with the cut running from $a$ to $+\infty$, the phase just above the real axis is $0$ to the right of $a$ and $\pi/2$ to the left of $a$. Just below the real axis it is $\pi$ to the right and $\pi/2$ to the left. Do the same for $(z-b)^{1/2}$.

For the product, the phases add. For the ratio, they subtract. With $M=\sqrt{|z-a||z-b|}$ this gives:

| Region (just above / just below the real axis) | $f=(z-a)^{1/2}(z-b)^{1/2}$ |
|---|---|
| right of $b$ | $+M$ (both sides) |
| left of $a$ | $-M$ (both sides) |
| between $a$ and $b$, above | $+iM$ |
| between $a$ and $b$, below | $-iM$ |

The phase only jumps between $a$ and $b$, so that segment is the cut. Outside it the contributions of the two factors cancel or add up consistently. Across the cut, $\operatorname{disc}f=2iM$.

For the ratio, the phases to the right of $b$ and to the left of $a$ cancel. Equivalently, $\big(\frac{z-a}{z-b}\big)^{1/2}\to1$ as $z\to\infty$, so the function is regular there.

**Worked example:**
Check $\infty$ for $\alpha\neq\frac12$. At large $z$ the product behaves like $z^{2\alpha}$, which is not single valued unless $2\alpha$ is an integer. So $\infty$ is a branch point and the cut cannot be closed off at a finite point. The finite cut for $\alpha=\tfrac12$ is a coincidence, because $z^{2\alpha}=z$ is regular. This is an exercise left in the notes for $\alpha\ne\frac12$, where the phases along the real axis come out as multiples of $\pi\alpha$ ($2\pi\alpha$, $\pi\alpha$, $3\pi\alpha$, $4\pi\alpha$ in the different regions).

**Pitfalls / conditions to watch:**
- Do not assume the half-integer case generalises. The finite cut for the product works only for $\alpha=\frac12$ (half-odd integers).
- The ratio with any non-integer $\alpha$ is fine on a finite cut.
- Phase angles of $2\pi$ and $0$ are equivalent, so keep track of the principal range chosen.

---

> ✍️ **Added by:** <your name(s)>, 2 Oct 2026

### Contour integrals with branch points: the keyhole (hairpin) contour

**Statement:**
For multivalued integrands the contour must be chosen so that the function returns to its starting value. Two strategies from the lecture:

1. Avoid encircling a single branch point, for example by going around both $a$ and $b$ or running the contour just above and below the cut.
2. Encircle several branch points, or the same one several times, until the function comes back to the original sheet.

A standard application is

$$\int_0^\infty \frac{x^{p-1}}{1+x}\,dx=\frac{\pi}{\sin \pi p},\qquad 0<p<1.$$

**Derivation / justification (condensed):**
Let $f(z)=\dfrac{z^{p-1}}{1+z}$. It has algebraic branch points at $0$ and $\infty$, and a simple pole at $z=-1$. Take the cut along the positive real axis, so $0\le\theta<2\pi$. Use the keyhole contour $C$: along the top of the cut from $\epsilon$ to $R$ (AB), the big circle (BD), back along the underside from $R$ to $\epsilon$ (DE), then the small circle around the origin.

- On AB, $\theta\approx0$, so we get $I=\int_0^\infty\frac{x^{p-1}}{1+x}dx$.
- On DE, $\theta\approx2\pi$, so $z^{p-1}$ picks up $e^{2\pi i(p-1)}=e^{2\pi i p}$. The direction is reversed, giving $-e^{2\pi ip}I$.
- The small circle contributes like $\epsilon^{p}\to0$, and the big circle like $R^{p-1}\to0$, both for $0<p<1$.
- Residue theorem: $\oint_C f\,dz=2\pi i\,\mathrm{Res}_{z=-1}f=2\pi i\,(-1)^{p-1}=-2\pi i\,e^{i\pi p}$.

So

$$I\,(1-e^{2\pi i p})=-2\pi i\,e^{i\pi p}\ \Longrightarrow\ I=\frac{-2\pi i}{e^{-i\pi p}-e^{i\pi p}}=\frac{\pi}{\sin\pi p}.$$

**Worked example:**
The notes also treat $\displaystyle\int_0^1 x^{1-p}(1-x)^{p}Q(x)\,dx$ with $Q$ rational and without poles on $0<x\le1$. The cut is the segment $[0,1]$. Write $\theta=\arg z$ and $\phi=\arg(z-1)$, both in $(0,2\pi)$. Then $\arg f$ just above the cut is $p\pi$ and just below it is $(2-p)\pi$. So

$$\operatorname{disc} f=2i\sin(p\pi)\,x^{1-p}(1-x)^{p}Q(x),$$

and the real integral equals $\dfrac{1}{-2i\sin p\pi}\oint_\Gamma z^{1-p}(z-1)^pQ(z)\,dz$.

Balakrishnan §26.1.3 uses the same trick with $\ln z$. Take $I'=-\frac{1}{2\pi i}\oint_C\frac{p(z)\ln z}{q(z)}dz$ on a hairpin around the positive real axis. Since $\ln z$ differs by $2\pi i$ between the two sides, $I'=\int_0^\infty p/q\,dx$. This works when $\deg q\ge\deg p+2$ and $q$ has no zeros for $x\ge0$. One consequence is

$$\int_0^\infty\frac{dx}{x^n+1}=\frac\pi n\csc\frac\pi n\quad(n=2,3,\dots).$$

**Pitfalls / conditions to watch:**
- Check the arcs vanish. The condition $0<p<1$ is exactly what kills both the small and the large circle.
- Fix the phase convention first. Using $0\le\theta<2\pi$ gives the factor $e^{2\pi ip}$ on the lower lip.
- The two straight pieces do not cancel. They differ by the phase factor, which is the whole point of the method.
- Do not shrink the contour across the cut. It must stay on the two lips.

---

> ✍️ **Added by:** <your name(s)>, 2 Oct 2026

### The Gamma function as a hairpin contour integral

**Statement:**
For all complex $z$ not a non-positive integer,

$$\Gamma(z)=\frac{1}{1-e^{2\pi i z}}\int_C t^{z-1}e^{-t}\,dt,$$

where $C$ comes in from $+\infty$ just below the positive real axis, goes round the origin in the negative sense and runs back out to $+\infty$ just above the axis.

**Derivation / justification (condensed):**
The factor $t^{z-1}$ has branch points at $t=0$ and $\infty$, with the cut on the positive real axis. Just above the cut its phase is $0$. Just below it is $2\pi z$, since $e^{-2\pi i}=1$.

For $\operatorname{Re}z>0$ the small arc around the origin vanishes. The two straight pieces give $\Gamma(z)$ on the upper lip and $-e^{2\pi iz}\Gamma(z)$ on the lower lip. So $I(z)=(1-e^{2\pi iz})\Gamma(z)$ there.

The contour does not pass through $t=0$, so it can be deformed away from the origin. That makes $I(z)$ defined for all finite $z$. The factor $(1-e^{2\pi iz})^{-1}$ has simple poles at the integers, and the product is meromorphic. This gives the analytic continuation of $\Gamma$ to the whole plane.

**Worked example:**
Two checks on the formula.

- At $z=n=1,2,\dots$, the integrand $t^{n-1}e^{-t}$ has no branch point, so the contour integral vanishes. That cancels the pole of $1/(1-e^{2\pi iz})$. The limit gives $(n-1)!$.
- At $z=-n$ for $n=0,1,2,\dots$, the cut disappears but there is a pole of order $n+1$ at $t=0$. Picking out the coefficient of $1/t$ gives a simple pole of $\Gamma$ at $z=-n$ with residue $(-1)^n/n!$.

**Pitfalls / conditions to watch:**
- The contour must end with $\operatorname{Re}t\to+\infty$ at both ends, so the factor $e^{-t}$ gives convergence.
- Because of that, you cannot close the hairpin with a large circle. That differs from the keyhole contour in the previous entry.
- The apparent poles at all integers are only real for $z\le0$.

---
