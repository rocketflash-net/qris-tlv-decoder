# QRIS TLV Decoder

Paste a QRIS payload and see every EMV tag split into tag, length and value, with what each field means.

**Live:** https://rocketflash-net.github.io/qris-tlv-decoder/

- Decodes root tags and nested templates (26–51 merchant account, 62 additional data, 64 language, 80–99)
- Verifies the CRC-16/CCITT-FALSE checksum (tag 63) and shows the expected value on mismatch
- Checks QRIS v1.9 rules: mandatory tags (incl. 51, 61, 62 and 62.08), field lengths, duplicates, tag order, tip consistency
- Recovers payloads where a value over 99 characters was written with a two-digit length, and flags it
- Explains values: static/dynamic, MCC, currency, merchant criteria (UMI/UKE/UME/UBE), merchant channel, NNS
- Links the colour-coded payload to the field list on hover
- English and Bahasa Indonesia, light and dark theme, copy result as JSON

Everything runs in the browser. The payload is never sent anywhere.

Reference: Standar Nasional QR Code Indonesia MPM (QRIS) v1.9 by ASPI, built on the EMVCo Merchant-Presented Mode spec. This is a learning and debugging tool, not an official validator.

---

Built by [Daniel Aldo Pratama](https://rocketflash-net.github.io/it/).
