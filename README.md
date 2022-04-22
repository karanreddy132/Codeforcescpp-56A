# Codeforcescpp-56A
#include <bits/stdc++.h>
using namespace std;

int main() {
	int n, count(0);
	string s;
	cin >> n;
	string arr[] = {"ABSINTH",
					"BEER",
					"BRANDY",
					"CHAMPAGNE",
					"GIN",
					"RUM",
					"SAKE",
					"TEQUILA",
					"VODKA",
					"WHISKEY",
					"WINE"};
	for (int i = 0; i < n; i++) {
		cin >> s;
		string *result = find(arr, arr + 11, s);
		if (!isalpha(s[0])) {
			if (stoi(s) < 18) {
				count++;
			}
		} else if (result != arr + 11) {
			count++;
		}
	}
	cout << count;
	return 0;
}
