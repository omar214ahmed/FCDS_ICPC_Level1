## Sum formulas

| Case | Formula |
|---|---|
| Odd numbers up to N (N odd) | ((N + 1) / 2)² |
| Even numbers up to N (N even) | (N / 2) × (N / 2 + 1) |
| All numbers 1 to N | N(N + 1) / 2 |

## C++ type sizes

### Signed

| Type | Bytes | Bits | Range |
|---|---|---|---|
| `bool` | 1 | 8 | `true` / `false` |
| `char` | 1 | 8 | -128 to 127 |
| `int16_t` (short) | 2 | 16 | -32,768 to 32,767 |
| `int32_t` (int) | 4 | 32 | -2,147,483,648 to 2,147,483,647 |
| `int64_t` (long long) | 8 | 64 | about ±9.2 quintillion |
| `float` | 4 | 32 | about 7 significant digits |
| `double` | 8 | 64 | about 15 significant digits |
| `std::string` | varies | varies | 1 byte per ASCII character (plus internal bookkeeping) |

### Unsigned

| Type | Bytes | Bits | Range |
|---|---|---|---|
| `unsigned char` | 1 | 8 | 0 to 255 |
| `unsigned short` | 2 | 16 | 0 to 65,535 |
| `unsigned int` | 4 | 32 | 0 to 4,294,967,295 |
| `unsigned long long` | 8 | 64 | 0 to 18,446,744,073,709,551,615 |

## Notes

- Sizes of `int`, `long` and `long double` can vary by platform, so the fixed-width types from `<cstdint>` (`int16_t`, `int32_t`, `int64_t`) are safer when you need an exact size.
- Add `unsigned` (or `uint32_t`, etc.) to shift the range to start at 0 and double the max, e.g. `uint32_t` goes from 0 to 4,294,967,295.