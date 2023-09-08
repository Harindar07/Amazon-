string longestCommonPrefix(vector<string> p) {
    if (p.size() == 0) return "";

    for (auto& str : p) {
        transform(str.begin(), str.end(), str.begin(), ::tolower);
    }

    string prefix = p[0];

    for (int i = 1; i < p.size(); ++i) {
        string s = p[i];
        if (s.size() == 0 || prefix == "") return "";
        prefix = prefix.substr(0, min(prefix.size(), s.size()));

        for (int k = 0; k < s.size() && k < prefix.size(); ++k) {
            if (s[k] != prefix[k]) {
                prefix = prefix.substr(0, k);
                break;
            }
        }
    }
    return prefix;
}