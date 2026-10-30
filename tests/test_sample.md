\# Test Results

Python version used: 3.13.2 | Operating system: Windows | Date: 29-Oct-2026

| # | Input | Expected result | Actual result | Pass/Fail |

|---|-------|-----------------|---------------|-----------|

| 1 | https://www.example.com/login | No listed warning signs | No listed warning signs found. | Pass |

| 2 | http://192.0.2.10/account | IP address + HTTP | Uses an IP address instead of a familiar domain and uses HTTP | Pass |

| 3 | http://example.com@sample.invalid/login | @ symbol + HTTP | Contains @ symbol and uses HTTP | Pass |

| 4 | https://a.b.c.d.e.example.invalid/path | Many hostname segments | Contains many hostname segments/subdomains. | Pass |

| 5 | https://xn--example.invalid/ | Punycode-style hostname | Contains a punycode-style hostname. | Pass |



Bonus Checks :

| 6 | Pressing Enter | No URL entered. | No URL entered. | Pass |

| 7 | www.example.com | Uses HTTP. HTTPS alone does not prove trust. | Uses HTTP instead of HTTPS | Pass |

| 8 | https://secure-login.example.invalid | No listed warning signs found. This does NOT prove safety. | No listed warning signs found. | Pass |

| 9 | http://\[bad | The program stops with ValueError: Invalid IPv6 URL | Invalid IPv6 URL | Pass |

Note: Added a try-except block to handle malformed URLs and prevent ValueError crashes. Test 9 improvised Result "This text is not a valid URL format."

