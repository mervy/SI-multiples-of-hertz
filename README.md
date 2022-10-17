The hertz (symbol: Hz) is the unit of frequency in the International System of Units (SI), equivalent to one event (or cycle) per second.[1][3] The hertz is an SI derived unit whose expression in terms of SI base units is s−1, meaning that one hertz is the reciprocal of one second.[2] It is named after Heinrich Rudolf Hertz (1857–1894), the first person to provide conclusive proof of the existence of electromagnetic waves. Hertz are commonly expressed in multiples: kilohertz (103 Hz, kHz), megahertz (106 Hz, MHz), gigahertz (109 Hz, GHz), terahertz (1012 Hz, THz).

Some of the unit's most common uses are in the description of sine waves and musical tones, particularly those used in radio- and audio-related applications. It is also used to describe the clock speeds at which computers and other electronics are driven. The units are sometimes also used as a representation of the energy of a photon, via the Planck relation E = hν, where E is the photon's energy, ν is its frequency, and the proportionality constant h is the Planck constant.

SI multiples of hertz (Hz)
Submultiples		Multiples
Value	SI symbol	Name	Value	SI symbol	Name
10−1 Hz	dHz	decihertz	101 Hz	daHz	decahertz
10−2 Hz	cHz	centihertz	102 Hz	hHz	hectohertz
10−3 Hz	mHz	millihertz	103 Hz	kHz	kilohertz
10−6 Hz	µHz	microhertz	106 Hz	MHz	megahertz
10−9 Hz	nHz	nanohertz	109 Hz	GHz	gigahertz
10−12 Hz	pHz	picohertz	1012 Hz	THz	terahertz
10−15 Hz	fHz	femtohertz	1015 Hz	PHz	petahertz
10−18 Hz	aHz	attohertz	1018 Hz	EHz	exahertz
10−21 Hz	zHz	zeptohertz	1021 Hz	ZHz	zettahertz
10−24 Hz	yHz	yoctohertz	1024 Hz	YHz	yottahertz

https://www.sololearn.com/Discuss/517483/1024-geop-byte

1 Bit = Binary Digit
8 Bits = 1 Byte
1024 Bytes = 1 Kilobyte
1024 Kilobytes = 1 Megabyte
1024 Megabytes = 1 Gigabyte
1024 Gigabytes = 1 Terabyte
1024 Terabytes = 1 Petabyte
1024 Petabytes = 1 Exabyte
1024 Exabytes = 1 Zettabyte
1024 Zettabytes = 1 Yottabyte
1024Yottabytes = 1 Brontobyte
1024 Brontobytes = 1 Geopbyte
1024 Geopbyte=1 Saganbyte
1024 Saganbyte=1 Pijabyte
Alphabyte = 1024 Pijabyte
Kryatbyte = 1024 Alphabyte
Amosbyte = 1024 Kryatbyte
Pectrolbyte = 1024 Amosbyte
Bolgerbyte = 1024 Pectrolbyte
Sambobyte = 1024 Bolgerbyte
Quesabyte = 1024 Sambobyte
Kinsabyte = 1024 Quesabyte
Rutherbyte = 1024 Kinsabyte
Dubnibyte = 1024 Rutherbyte
Seaborgbyte = 1024 Dubnibyte
Bohrbyte = 1024 Seaborgbyte
Hassiubyte = 1024 Bohrbyte
Meitnerbyte = 1024 Hassiubyte
Darmstadbyte = 1024 Meitnerbyte
Roentbyte = 1024 Darmstadbyte
Coperbyte = 1024 Roentbyte

---
stage: Monitor
group: Respond
info: To determine the technical writer assigned to the Stage/Group associated with this page, see https://about.gitlab.com/handbook/product/ux/technical-writing/#assignments
---

# Unit formats reference **(FREE)**

> [Introduced](https://gitlab.com/gitlab-org/gitlab/-/issues/201999) in GitLab 12.9.

Format the data in your dashboard panels.

You can select units to format your charts by adding `format` to your
[axis configuration](yaml.md).

## Internationalization and localization

Currently, your [internationalization and localization options](https://en.wikipedia.org/wiki/Internationalization_and_localization) for number formatting are dependent on the system you are using (that is, your OS or browser).

## Engineering Notation

For generic or default data, numbers are formatted according to the current locale in [engineering notation](https://en.wikipedia.org/wiki/Engineering_notation).

While an [engineering notation exists for the web](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Intl/NumberFormat), GitLab uses a version based off the [scientific notation](https://en.wikipedia.org/wiki/Scientific_notation). GitLab formatting acts in accordance with SI prefixes. For example, using GitLab notation, `1500.00` becomes `1.5k` instead of `1.5E3`. Keep this distinction in mind when using the engineering notation for your metrics.

Formats: `engineering`

SI prefixes:

| Name       | Symbol  | Value                      |
| ---------- | ------- | -------------------------- |
| `yotta`    | Y       | 1000000000000000000000000  |
| `zetta`    | Z       | 1000000000000000000000     |
| `exa`      | E       | 1000000000000000000        |
| `peta`     | P       | 1000000000000000           |
| `tera`     | T       | 1000000000000              |
| `giga`     | G       | 1000000000                 |
| `mega`     | M       | 1000000                    |
| `kilo`     | k       | 1000                       |
| `milli`    | m       | 0.001                      |
| `micro`    | μ       | 0.000001                   |
| `nano`     | n       | 0.000000001                |
| `pico`     | p       | 0.000000000001             |
| `femto`    | f       | 0.000000000000001          |
| `atto`     | a       | 0.000000000000000001       |
| `zepto`    | z       | 0.000000000000000000001    |
| `yocto`    | y       | 0.000000000000000000000001 |

**Examples:**

| Data                              | Displayed |
| --------------------------------- | --------- |
| `0.000000000000000000000008`      | 8y        |
| `0.000000000000000000008`         | 8z        |
| `0.000000000000000008`            | 8a        |
| `0.000000000000008`               | 8f        |
| `0.000000000008`                  | 8p        |
| `0.000000008`                     | 8n        |
| `0.000008`                        | 8μ        |
| `0.008`                           | 8m        |
| `10`                              | 10        |
| `1080`                            | 1.08k     |
| `18000`                           | 18k       |
| `18888`                           | 18.9k     |
| `188888`                          | 189k      |
| `18888888`                        | 18.9M     |
| `1888888888`                      | 1.89G     |
| `1888888888888`                   | 1.89T     |
| `1888888888888888`                | 1.89P     |
| `1888888888888888888`             | 1.89E     |
| `1888888888888888888888`          | 1.89Z     |
| `1888888888888888888888888`       | 1.89Y     |
| `1888888888888888888888888888`    | 1.89e+27  |

## Numbers

For number data, numbers are formatted according to the current locale.

Formats: `number`

**Examples:**

| Data  | Displayed |
| ---------- | --------- |
| `10`       | 1         |
| `1000`     | 1,000     |
| `1000000`  | 1,000,000 |

## Percentage

For percentage data, format numbers in the chart with a `%` symbol.

Formats supported: `percent`, `percentHundred`

**Examples:**

| Format           | Data  | Displayed |
| ---------------- | ----- | --------- |
| `percent`        | `0.5` | 50%       |
| `percent`        | `1`   | 100%      |
| `percent`        | `2`   | 200%      |
| `percentHundred` | `50`  | 50%       |
| `percentHundred` | `100` | 100%      |
| `percentHundred` | `200` | 200%      |

## Duration

For time durations, format numbers in the chart with a time unit symbol.

Formats supported: `milliseconds`, `seconds`

**Examples:**

| Format         | Data   | Displayed |
| -------------- | ------ | --------- |
| `milliseconds` | `10`   | 10ms      |
| `milliseconds` | `500`  | 100ms     |
| `milliseconds` | `1000` | 1000ms    |
| `seconds`      | `10`   | 10s       |
| `seconds`      | `500`  | 500s      |
| `seconds`      | `1000` | 1000s     |

## Digital (Metric)

Converts a number of bytes using metric prefixes. It scales to
use the unit that's the best fit.

Formats supported:

- `decimalBytes`
- `kilobytes`
- `megabytes`
- `gigabytes`
- `terabytes`
- `petabytes`

**Examples:**

| Format         | Data      | Displayed |
| -------------- | --------- | --------- |
| `decimalBytes` | `1`       | 1B        |
| `decimalBytes` | `1000`    | 1kB       |
| `decimalBytes` | `1000000` | 1MB       |
| `kilobytes`    | `1`       | 1kB       |
| `kilobytes`    | `1000`    | 1MB       |
| `kilobytes`    | `1000000` | 1GB       |
| `megabytes`    | `1`       | 1MB       |
| `megabytes`    | `1000`    | 1GB       |
| `megabytes`    | `1000000` | 1TB       |

## Digital (IEC)

Converts a number of bytes using binary prefixes. It scales to
use the unit that's the best fit.

Formats supported:

- `bytes`
- `kibibytes`
- `mebibytes`
- `gibibytes`
- `tebibytes`
- `pebibytes`

**Examples:**

| Format      | Data          | Displayed |
| ----------- | ------------- | --------- |
| `bytes`     | `1`           | 1B        |
| `bytes`     | `1024`        | 1KiB      |
| `bytes`     | `1024 * 1024` | 1MiB      |
| `kibibytes` | `1`           | 1KiB      |
| `kibibytes` | `1024`        | 1MiB      |
| `kibibytes` | `1024 * 1024` | 1GiB      |
| `mebibytes` | `1`           | 1MiB      |
| `mebibytes` | `1024`        | 1GiB      |
| `mebibytes` | `1024 * 1024` | 1TiB      |


