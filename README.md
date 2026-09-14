def compress_text(text):
    result = []
    count = 1

    for i in range(1, len(text) + 1):
        if i < len(text) and text[i] == text[i - 1]:
            count += 1
        else:
            result.append(text[i - 1] + str(count))
            count = 1

    return "".join(result)


if __name__ == "__main__":
    text = "aaabbccccd"
    print("Original:", text)
    print("Compressed:", compress_text(text))
