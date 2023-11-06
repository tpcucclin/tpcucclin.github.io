# Markdown Cheat Sheet

Thanks for visiting [The Markdown Guide](https://www.markdownguide.org)!

This Markdown cheat sheet provides a quick overview of all the Markdown syntax elements. It can’t cover every edge case, so if you need more information about any of these elements, refer to the reference guides for [basic syntax](https://www.markdownguide.org/basic-syntax/) and [extended syntax](https://www.markdownguide.org/extended-syntax/).

## Basic Syntax

These are the elements outlined in John Gruber’s original design document. All Markdown applications support these elements.

### Heading

# H1
## H2
### H3

### Bold

**bold text**

### Italic

*italicized text*

### Blockquote

> blockquote

### Ordered List

1. First item
2. Second item
3. Third item

### Unordered List

- First item
- Second item
- Third item

### Code

#### 解決背包問題(Python程式碼)，使用動態規劃方法：

```Python
def knapsack(weights, values, capacity):
    n = len(values)
    # dp = [[0 for _ in range(capacity + 1)] for _ in range(n + 1)]
    dp = [[0] * (capacity+1) for _ in range(n + 1)]

    for i in range(1, n + 1):
        for j in range(1, capacity + 1):
            w,v = weights[i-1],values[i-1]
            if w > j:
                dp[i][j] = dp[i-1][j]
            else:
                dp[i][j] = max(dp[i-1][j], dp[i-1][j-w] + v)

    return dp[n][capacity]

# Example input
weights = [3,4,7,3,2]
values = [4,5,10,8,6]
capacity = 10

print("Maximum value that can be obtained:", knapsack(weights, values, capacity))
```


### Horizontal Rule

---

### Link

[Markdown Guide](https://www.markdownguide.org)

### Image

![alt text](https://www.markdownguide.org/assets/images/tux.png)

## Extended Syntax

These elements extend the basic syntax by adding additional features. Not all Markdown applications support these elements.

### Table

| Syntax | Description |
| ----------- | ----------- |
| Header | Title |
| Paragraph | Text |

### Fenced Code Block

```JSON
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```

### Footnote

Here's a sentence with a footnote. [^1]

[^1]: This is the footnote.

### Heading ID

### My Great Heading {#custom-id}

### Definition List

term
: definition

### Strikethrough

~~The world is flat.~~

### Task List

- [x] Write the press release
- [ ] Update the website
- [ ] Contact the media

### Emoji

That is so funny! :joy:

(See also [Copying and Pasting Emoji](https://www.markdownguide.org/extended-syntax/#copying-and-pasting-emoji))

### Highlight

I need to highlight these ==very important words==.

### Subscript

H<sub>2</sub>O, CO<sub>2</sub>

### Superscript

*3X<sup>2</sup> + 2X + 3 = 10*

### Markdown+Math

$x^2+2x+3$ 

$\int_0^\infty \frac{x^3}{e^x-1}\,dx = \frac{\pi^4}{15}$

Write normal distribution in Latex

$f(x) = \frac{1}{\sigma\sqrt{2\pi}}\exp\left( -\frac{1}{2}\left(\frac{x-\mu}{\sigma}\right)^{\!2}\,\right)$

$f(x)=\frac{1}{{\sigma\sqrt{2\pi}}}e^{-\frac{(x-\mu)^{2}}{2\sigma^{2}}}$

$X \sim \mathcal{N}(\mu,\sigma^2)$

$f(x)=\frac{1}{\sigma\sqrt{2\pi}}\exp{[-\frac{(x-\mu)^{2}}{2\sigma^{2}}]}$