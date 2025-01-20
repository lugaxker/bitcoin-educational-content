---
term: DLP (DISCREET LOG PROBLEM)

---
Das Diskrete Logarithmus-Problem (DLP) ist ein mathematisches Problem, das die Sicherheit von kryptographischen Algorithmen mit öffentlichem Schlüssel untermauert, insbesondere die in Bitcoin verwendeten. Wenn es in einer zyklischen Gruppe der Ordnung $q$ mit einem Generator $g$ eine Gleichung der Form $g^x = h$ gibt, dann nennt man $x$ den diskreten Logarithmus von $h$ in Bezug auf die Basis $g$, modulo $q$. Vereinfacht gesagt, geht es darum, den Exponenten $x$ zu bestimmen, wenn $g$, $h$ und $q$ bekannt sind. Der diskrete Logarithmus ist also die Umkehrung des Exponentials in einer endlichen zyklischen Gruppe. Für große Werte von $q$ gilt die Lösung des diskreten Logarithmusproblems jedoch als algorithmisch schwierig. Diese Eigenschaft wird ausgenutzt, um die Sicherheit vieler kryptographischer Protokolle zu gewährleisten, z. B. des Diffie-Hellman-Protokolls für den Schlüsselaustausch. Der diskrete Logarithmus wird auch in der Kryptographie mit elliptischen Kurven (ECC) verwendet, unter anderem im Elliptic Curve Digital Signature Algorithm (ECDSA). Im Zusammenhang mit elliptischen Kurven besteht das Problem des diskreten Logarithmus darin, einen Skalar $k$ zu finden, der so beschaffen ist, dass $k \cdot G = K$, wobei $G$ und $K$ Punkte auf der Kurve sind und $\cdot$ die Punktmultiplikationsoperation darstellt. Im Kontext von Bitcoin verwenden Standardtransaktionen entweder ECDSA oder das Schnorr-Protokoll, um UTXOs zu sperren. Beide beruhen auf der Unmöglichkeit, den diskreten Logarithmus zu berechnen.