# python-data-assignments

# DISCUSSION
# I choose the first way, that is to assemble the content of all 5 files and extract keyword list for one string. It is simple and convenient to put all files into one and execute codes on the data of all file in the case where all texts are available for me.

# From the perspective of further future reuse, however, I think it's better to extract keyword-frequency list for all 5 files first and then merge the keyword-frequency. Because a file is viewed as one parameter every time and we just need to add up all results returned after the implements of functions. Also, in this way, we can locate the keywords in the articles accurately and quickly.

# WORKING DEMO
def extract_key_words_1(file_1):
# 1. Read one .txt file in folder assignment0/.
    f = open (file_1,'r')     
    content = f.read()

# 2. Remove all punctuations and extract the English words from the file content.
    import re
    punctuation='[\s+\.\!\/_,$%^*(+\"\')]+|[+——()?:【】“”‘’！，。？、~@#￥%……&*（）]+'
    read_file = re.sub(punctuation,' ',content)
    extract_words = read_file.lower().split() 

# 3. Handle the stop words
    stop_words = ["i", "me", "my", "myself", "we", "our", "ours"...]
    new_list = []
    for w in extract_words:
        if w not in stop_words:
            new_list.append(w)

# 4. For every word extracted above, count how many times each one appears
    count_word_1={}
    for word in new_list:
        if word not in count_word_1:
            count_word_1[word] = 1
        else:
            count_word_1[word] += 1
    return count_word_1

# 5. Merge the dictionaries of keyword-frequency and rank the keywords from higher frequency to lower frequency
def merge_key_words(count_word_1, count_word_2...):
    all_word = {**count_word_1, **count_word_2...}
    import operator
    rank_word = sorted(all_word.items(), key=operator.itemgetter(1),reverse=True)
    return(rank_word[0:15])