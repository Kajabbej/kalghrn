{
 "cells": [
  {
   "cell_type": "markdown",
   "id": "19d1d50c",
   "metadata": {},
   "source": [
    "# tugas dekomposisi QR"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "f10e02e8",
   "metadata": {},
   "source": [
    "\n",
    "## Foto Catatan\n",
    "\n",
    "::::{grid} 3\n",
    ":::{grid-item}\n",
    "![Bagian 1](images/Dekomposisi/1.jpeg)\n",
    "\n",
    "**Bagian 1** — Setup & $q_1$\n",
    ":::\n",
    ":::{grid-item}\n",
    "![Bagian 2](images/Dekomposisi/2.jpeg)\n",
    "\n",
    "**Bagian 2** — Kolom $a_4$\n",
    ":::\n",
    ":::{grid-item}\n",
    "![Bagian 3](images/Dekomposisi/3.jpeg)\n",
    "\n",
    "**Bagian 3** — $v_2$, $q_2$, $v_3$\n",
    ":::\n",
    "::::\n",
    "\n",
    "---\n",
    "\n",
    "## Keterangan Bagian 1\n",
    "\n",
    "$$A = \\begin{bmatrix} 3 & -2 & 5 & 1 \\\\ 0 & 4 & -1 & 2 \\\\ -3 & 1 & 2 & -4 \\\\ 2 & 0 & -2 & 3 \\end{bmatrix}$$\n",
    "\n",
    "$$\\|v_1\\| = \\sqrt{22}, \\quad q_1 = \\frac{1}{\\sqrt{22}}\\begin{bmatrix}3\\\\0\\\\-3\\\\2\\end{bmatrix}$$\n",
    "\n",
    "$$R_{11} = \\sqrt{22}, \\quad a_2 \\cdot q_1 = \\frac{-9}{\\sqrt{22}}$$\n",
    "\n",
    "$$v_2 = \\begin{bmatrix}-2\\\\4\\\\1\\\\0\\end{bmatrix} - \\frac{-9}{\\sqrt{22}} \\cdot \\frac{1}{\\sqrt{22}}\\begin{bmatrix}3\\\\0\\\\-3\\\\2\\end{bmatrix}$$\n",
    "\n",
    "---\n",
    "\n",
    "## Keterangan Bagian 2\n",
    "\n",
    "$$R_{14} = \\frac{1}{\\sqrt{22}}(3+0+12+6) = \\frac{21}{\\sqrt{22}}$$\n",
    "\n",
    "$$v_4 = a_4 - \\sum_{j=1}^{3}(a_4 \\cdot q_j)q_j$$\n",
    "\n",
    "---\n",
    "\n",
    "## Keterangan Bagian 3\n",
    "\n",
    "$$v_2 = \\begin{bmatrix}-\\frac{17}{22}\\\\4\\\\-\\frac{5}{22}\\\\\\frac{18}{22}\\end{bmatrix}, \\quad q_2 = \\frac{v_2}{\\|v_2\\|}$$\n",
    "\n",
    "$$R_{13} = \\frac{1}{\\sqrt{22}}(15-0-6-4) = \\frac{5}{\\sqrt{22}}$$\n",
    "\n",
    "$$q_3 = \\frac{v_3}{\\|v_3\\|}$$"
   ]
  }
 ],
 "metadata": {
  "language_info": {
   "name": "python"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 5
}
