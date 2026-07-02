# Markdown

Markdown is a lightweight markup language that allows you to format text using plain characters. It’s widely used for README files, documentation, and Jupyter 
Notebooks. For better experience, install "Markdown All in One" extension from the sidebar.

- Press `⌘ + Shift + V` (Mac) or `Ctrl + Shift + V` (Windows) to see preview (how it renders). Repress to close.
- Press `⌘ + K` then `V` (Mac) or `Ctrl + K` then `V` (Windows) to see live side preview. Repress to close.

Your website pages will be created from `.md` file.

Markdown ignores single line breaks by default.
To create a new paragraph or visible line break, press Enter twice (i.e., leave a blank line), 

not just one.

> You can even type emojis like 😎

## Headings

Use `#` for headings. The number of `#` symbols indicates the level.

# Heading 1
## Heading 2
### Heading 3

#### Heading 4

## 1. Emphasis

Italic: *text* (With extension, shortcut: `⌘ + I` (Mac) or `Ctrl + I` (Windows))

Bold: **text** (With extension, shortcut: `⌘ + B` (Mac) or `Ctrl + B` (Windows))

Bold & Italic: ***text***

## 2. List

#### Unordered list
- Item 1
- Item 2
  - Subitem
    - Subsubitem

#### Ordered list
1. Item
    1. Subitem
    2. Subitem
2. Item
    1. Subitem

#### ✅ Task list
- [x] Install Git
- [x] Install Python
- [ ] Drink milk

## 3. Quote
> This is important.

## 4. Link
#### Link to external website
Markdown Guide: <https://www.markdownguide.org>

Click [here](https://en.wikipedia.org/wiki/Markdown) to see get more info.

#### Link to internal section
- [here](#-list)
- [there](#-unordered-list)

## 5. Horizontal line
---

## 6. Code
#### Inline
`print("Hello, World!")`

#### Display / multiline
```python
    print("Hello, World!")
```

```python
    print("ABC")
    print("DEF")
```

## 7. $\LaTeX$
#### Inline
With extension, shortcut: `⌘ + M` (Mac) or `Ctrl + M` (Windows).

$xyz$, $ABC$, $\hat{a}$, $\tilde{b}$, $\dot{c}$, $\alpha$, $\infty$, $=$, $\neq$, $\approx$, $\sim$, $\le$, $<$, $\frac{3x}{5y}$, $\sqrt{x}$, $\sum_{i=1}^{n} x_i$, $\int_{0}^{1} x dx$.

You can find the commands for symbols from [here](https://detexify.kirelabs.org/classify.html#google_vignette). Guess how this website works.

#### Display
$$
y = \beta_{0} + \beta_{1} x + \beta_{2} x^{2}.
$$

$$
a^{2} + b^{2} = c^{2}.
\tag{1}
$$

$$
A = \begin{bmatrix}
1 & 2 & 3 \\
4 & 5 & 6
\end{bmatrix}.
$$

$$
\begin{gathered}
z = (x+y)^{2} \\
= x^{2} + 2xy + y^{2}.
\end{gathered}
$$

$$
\begin{aligned}
z &= (x+y)^{2} \\
&= x^{2} + 2xy + y^{2}.
\end{aligned}
$$



---

Later, we will learn how to include image and table.

