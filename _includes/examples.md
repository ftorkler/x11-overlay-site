<div markdown="1" class="examples">
# Examples

## Ansi Color Example

To colorize a text line or just a single word the well known ansi escape codes can be used like it's common for text in a terminal.

For example selecting red as a foreground font color can be achieved by using one of three different ansi color codes:
* <span class="sgr">[91</span> selects "Bright Red" out of a 16 color palette (4bit)
* <span class="sgr">[38;5;9</span> selects "Intense Red" out of a 256 color palette (8bit)
* <span class="sgr">[38;2;255;0;0</span> use "Red" color from RGB colors (24bit)

![example console command](/assets/images/example_color_console_echo.webp)

By using multiple sequences in a single line, something more advanded can be achieved. Using
"<span class="sgr">[91</span>CRIT<span class="sgr">[38;5;248</span>: Disk Space Usage (<span class="sgr">[97</span>96%<span class="sgr">[38;5;248</span>)<span class="sgr">[0</span>" for instance can be used to generate a critical alarm message with some details. The provided example file in the docs folder results to:
![example console command](/assets/images/example_color_console_cat.webp)

What you see in the console above is what you get with x11-overlay.
```
$> x11-overlay \
    docs/example-alarms.utf8.ans
```
![example console command](/assets/images/example_color_overlay.webp)

## Ansi Font Example

The default font can be set with the option <span class="option-param">-f, \--font-name=FONT</span> and the default font size with the option <span class="option-param">-s, \--font-size=SIZE</span>. Beside the primary default font, it's possible to select alternative fonts by using the ansi control sequence <span class="sgr">[11</span> to <span class="sgr">[19</span> whereever wanted. <span class="sgr">[10</span> selects the primary font again.

```
./bin/overlay -s 12,18 -f NotoSansMono,JetBrainsMono \
    docs/example-alarms.utf8.ans
```
![example console command](/assets/images/example_font_overlay.webp)
</div>
