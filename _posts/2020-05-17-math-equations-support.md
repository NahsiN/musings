# Corolla vs Ferrari

Imagine racing your car against an F1 car. Your car has speed $100~km/h$
while the F1 car has speed $300~km/h$. The race director decides to show mercy
and gives your car a head start. How long will it take for the F1 car
to catch up to you?

Denote $t_0$ as the head start given to your car. Your car travels a distance $d$ as,
\begin{equation}
  \label{eq:car}
  d = 100t,
\end{equation}
and the F1 car will travel that same distance as,
\begin{equation}
  \label{eq:f1}
  d = 300(t - t_0).
\end{equation}

Substituting \eqref{eq:car} into \eqref{eq:f1} and solving for $t$ gives
\begin{aligned}
  100t &= 300(t - t_0), \\
  200t &= 300t_0, \\
  \label{eq:t}
  t &= \frac{3}{2}t_0.         
\end{aligned}

Now, let's do a drag race! Let the drag strip be a $1~km$ long straight. What is the
head start your car requires to tie or win the race?

Substituting \eqref{eq:t} into \eqref{eq:car}, we've
\begin{equation}
  \label{eq:d}
  d = 150t_0.
\end{equation}
We plug in the numbers to get $t_0 = 1/150~h = 24~s$. Therefore, your car
needs to have a head start of at least $24~s$ to tie or win.
