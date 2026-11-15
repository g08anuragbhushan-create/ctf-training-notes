# Forensics — Cheatsheet

## File identification
- `file x`, `xxd x | head`, `binwalk x`, `exiftool x`, `pngcheck -v x`

## Carving
- `binwalk -e`, `foremost`, `photorec`, `TestDisk`

## Steganography
- images: `zsteg -a x.png`, `steghide extract -sf x.jpg`
- audio: Audacity spectrogram / Sonic Visualiser
- `strings` always first

## PCAP
- Wireshark: Statistics, follow TCP/HTTP streams, Export Objects
- `tshark -r x.pcap -Y http -T fields -e http.request.uri`

## Memory (Volatility)
- `volatility -f mem.raw imageinfo`
- `volatility -f mem.raw --profile=PROFILE pslist`
- `volatility -f mem.raw --profile=PROFILE filescan | grep -i flag`

## Gotchas
- Magic bytes vs extension mismatch
- Trailing data after PNG IEND often hides a zip
