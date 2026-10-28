# Ionic and Covalent Bonding

An interactive page for high school chemistry. Pick two elements on the periodic table and
watch the bond form, drawn as Lewis dot diagrams:

- **Metal + nonmetal → ionic.** The metal's valence electrons fly over to the nonmetal one at
  a time. The metal shrinks to a cation, the nonmetal gets brackets and a charge, and the
  formula comes from balancing the charges (Mg₃N₂, Al₂O₃, CaCl₂…).
- **Nonmetal + nonmetal → covalent.** The atoms slide together, their circles overlap, and
  each atom's unpaired electrons move into the overlap as shared pairs: single, double
  (CO₂), or triple (N₂) bonds. Lone pairs stay put.

Electrons are colored by the atom they came from, so students can see that a shared pair
has one electron from each atom and that an anion's extra electrons came from the metal.
A panel beside the drawing explains each step and counts the electrons around every atom.

**Live:** https://fractalated.github.io/Ionic-and-Covalent-Bonding/

## Only pairs that follow the simple rules

After the first pick, only elements that bond with it by these rules can be clicked
(they're outlined). 107 pairs are included: 70 ionic and 37 covalent.

- **Metals:** Li, Na, K, Rb, Cs, Mg, Ca, Sr, Ba, Al. **Nonmetals:** H, C, N, O, F, P, S, Cl,
  Se, Br, I. Everything else is greyed out.
- Left out on purpose: beryllium (its compounds are covalent); aluminum with anything but
  O and F (AlCl₃, Al₂S₃, AlN are largely covalent); nitrides of Na–Cs (not stable); metal
  hydrides, carbides, and phosphides; nonmetal pairs where the octet rule doesn't predict
  the real molecule (N + O, S + O, P + O, C + N, S + F) or the molecule is unstable (NBr₃,
  NI₃); and C, P, S, Se bonded to themselves (chains and rings).
- Every formula shown is a real compound. The covalent molecules are a fixed list in the
  code (`COV`); ionic formulas are computed from the charges.

The page was checked by running every allowed pair and confirming that the right number of
electrons is drawn, every nonmetal ends with 8 around it (hydrogen 2), every metal ion
ends with none, the charges cancel, and no two dots overlap.

## Running and linking

One self-contained `index.html`, no build step (Google Fonts only). Open it in a browser.

A pair can be linked directly: `…/Ionic-and-Covalent-Bonding/#Mg-N` opens magnesium nitride.

The page starts in dark mode; the button at the top right switches to light mode and is
remembered per browser. Animations are skipped for anyone whose system asks for reduced
motion.

## Deployment

GitHub Pages serves `index.html` from the `main` branch root. Pushing to `main` republishes
the site within a minute or two. The empty `.nojekyll` file skips the Jekyll build step.
