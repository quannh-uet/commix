## Version 1.2 (upcoming)
* Revised: The Windows-based payloads for every supported technique, had been shortly revised.
* Revised: The dynamic code evaluation ("eval-based") technique has been shortly revised.
* Added: New tamper script "space2tab.py" that replaces every space (" ") with plus ("%09").
* Added: The ability for generating powershell attack vectors via TrustedSec's Magic Unicorn.
* Added: The ability for checking if there is a new version available.
* Added: The ability for target application extension recognition (i.e PHP, ASP etc).
* Fixed: Minor improvement for finding the URL part (i.e scheme:[//host[:port]][/]path).
* Fixed: Minor fix for conflicted shells (i.e regular, alternative) from session file.

## Version 1.1 (2016-07-14)
* Added: The ".gitignore" file has been added.
* Added: Support for injections against ASP.NET applications.
* Added: Support for warning detection regarding "create_function()" function.
* Fixed: Minor improvent of the HTTP server for "--file-upload" option.
* Fixed: Minor fix for conflicted executed commands from session file in HTTP Headers.
* Added: The ability to store injection level into session files for current target. 
* Added: Support for automated enabling of an HTTP server for "--file-upload" option.
* Fixed: Minor fix for "Python-urllib" User-Agent exposure.

## Version 1.0 (2016-06-14)
* Revised: Time-relative statistical analysis for recognition of unexpected time delays due to unstable requests.
* Added: A list of pages / scripts potentially vulnerable to shellshock.
* Added: The ability to check if the url is probable to contain script(s) vulnerable to shellshock.
* Revised: Multiple eye-candy revisions have been performed.
* Fixed: HTTPS requests fixation, if the "--proxy" option is enabled.
* Fixed: Multiple fixes regarding the shellshock module have been performed.

## Version 0.9b (2016-06-07)
* Added: The ability to re-perform the injection request if it has failed.
* Fixed: The shell output in semiblind ("file-based") technique has been fixed not to concat new lines.
* Revised: The ability to execute multiple tamper scripts combined or the one after the other.
* Added: New tamper script "space2plus.py" that replaces every space (" ") with plus ("+").
* Added: New state ("checking") and the color of that state has been setted.
* Replaced: The "--base64" option has been replaced with "base64encode.py" tamper script.
* Added: New tamper script "space2ifs.py" that replaces every space (" ") with $IFS (bash) variable.
* Added: New option "--tamper" that supports tamper injection scripts.
* Added: Support for verbosity levels (currently supported levels: 0,1).
* Fixed: Minor rearrangement of prefixes and separators has been implemented.
* Revised: The "time-based" (blind) technique for *nix targets has been shortly revised.
* Revised: The source code has been revised to support "print_state_msg" (i.e error, warning, success etc) functions.

## Version 0.8b (2016-05-06)
* Fixed: The "--file-read" option to ignore the carriage return ("\r") character in a text file.
* Added: The ability to check for empty value(s) in the defined GET/POST/Cookie(s) data and skip.
* Replaced: The "INJECT_HERE" tag has been replaced with the "*" (asterisk) wildcard character.
* Added: New option "--level" (1-3) that specifies level of tests to perform.
* Added: New option "-p" that specifies a comma-separated list of GET/POST parameter.
* Added: The ability to check every parameter in the provided cookie data.
* Added: The ability to check every GET parameter in the defined URL and/or every POST provided data.
* Added: New option "--all" that enables all supported enumeration options.

## Version 0.7b (2016-04-18)
* Fixed: HTTP proxy logs parser to accept GET http requests.
* Fixed: HTTP proxy logs parser to recognise provided HTTP authentication credentials.
* Added: Support for verbose mode in HTTP authentication (Basic / Digest) dictionary-based cracker.
* Added: The ability to store valid (Digest) credentials into session files for current target.
* Added: Dictionary-based cracker for "Digest" HTTP authentication credentials.
* Added: Support for "Digest" HTTP authentication type.

## Version 0.6b (2016-04-01)
* Added: The ability to store valid (Basic) credentials into session files for current target.
* Added: New option "--ignore-401" that ignores HTTP Error 401 (Unauthorized) and continues tests without providing valid credentials.
* Added: Dictionary-based cracker for "Basic" HTTP authentication credentials.
* Added: Identifier for HTTP authentication type (currently only "Basic" type is supported).
* Added: New option "--skip-waf" that skips heuristic detection of WAF/IPS/IDS protection.
* Added: Support for verbose mode in the "DNS exfiltration" injection technique (module).
* Added: New option "--dns-server" that supports the "DNS exfiltration" injection technique (module).
* Added: New option "--dependencies" that checks (non-core) third party dependenices.

## Version 0.5b (2016-03-16)
* Fixed: The payload(s) for dynamic code evaluation ("eval-based"), if there is not any separator.
* Added: Support for verbose mode in the "ICMP exfiltration" injection technique (module). 
* Added: Check if the user-defined os name, is different than the one identified by heuristics.
* Added: New option "--os" that forces a user-defined os name.
* Added: Support for testing custom HTTP headers (via "--headers" parameter).

## Version 0.4.1b (2016-02-26)
* Added: Support for storing and retrieving executed commands from session file.
* Added: New option "-s" for loading session from session file.
* Added: New option "--ignore-session" for ignoring results stored in session file.
* Added: New option "--flush-session" for flushing session files for current target.
* Added: Support to resume to the latest injection points from session file.

## Version 0.4b (2016-02-04)
* Added: Payload mutation if WAF/IPS/IDS protection is detected.
* Added: Check for existence of WAF/IPS/IDS protection (via error pages).
* Added: The "set" option in "reverse_tcp" which sets a context-specific variable to a value.
* Added: New option "--force-ssl" for forcing usage of SSL/HTTPS requests.

## Version 0.3b (2016-01-15)
* Added: Time-relative false-positive identification, which identifies unexpected time delays due to unstable requests.
* Added: New option "-l", that parses target and data from HTTP proxy log file (i.e Burp or WebScarab).
* Added: Check if Powershell is enabled in target host, if the applied option's payload is requiring the use of PowerShell.
* Added: New option "--ps-version", that checks PowerShell's version number.
* Replaced: Some powershell-based payloads, have been replaced by new (more solid) ones, so to avoid "Microsoft-IIS" server's incompatibilities.
* Added: Support (in MacOSX platforms) for a tab completion in shell options.
* Added: Undocumented parameter "-InputFormat none" so to avoid "Microsoft-IIS" server's hang.
* Added: Ability for identification of "Microsoft-IIS" servers.
* Added: Statistical checks for time-related ("time-based"/"tempfile-based") techniques.
* Added: Support for Windows-based (cmd / powershell) payloads for every injection technique.

## Version 0.2b (2015-12-18)
* Added: Support for recalling previous commands.
* Added: Support (in Linux platforms) for tab completion in shell options.
* Added: Support for alternative (Python) os-shell in dynamic code evaluation ("eval-based") technique.
* Added: Support for PHP/Python meterpreter on "reverse_tcp" shell option.
* Added: The "reverse_tcp" shell option.
* Added: The ability to check for default root directories (Apache/Nginx).
* Added: Support for removal of (txt) shell files in semiblind ("file-based"/"tempfile-based") techniques.
* Added: Support for JSON POST data.
* Added: The "enumeration" and "file-read" results to log file.
* Added: The ability to get the user's approval before re-{enumerate/file-read} target.
* Added: The ability to stop current injection technique and proceed on the next one(s).

## Version 0.1b (2015-09-20)
* Added: New eval-based payload for "str_replace()" filter bypass.
* Added: Check for (GET) RESTful URL format.
* Added: New option "--base64", that encodes the OS command to Base64 format. 
* Added: Support for regular "preg_replace()" injections via "/e" modifier.
* Added: Support for HTML Charset and HTTP "Server" response-header reconnaissance (on verbose mode).
* Replaced: Payloads for "tempfile-based" (semiblind) technique, have been replaced by new (more solid) ones.
* Added: A "new-line" separator support, for "time-based" (blind) & "tempfile-based" (semiblind) techniques.
* Added: Support for referer-based command injections.
* Added: Support for user-agent-based command injections.
* Added: CVE-2014-6278 support for "shellshock" module.
* Added: Support for cookie-based command injections.
* Added: A generic false-positive prevention technique.
* Removed: The "Base64" detection option.
* Added: Support for the Tor network.
* Added: The "shellshock" (CVE-2014-6271) injection technique (module).
* Added: Termcolor support for Windows (colorama).
* Added: File access options.
* Added: Enumeration options.
* Added: New option "--alter-shell" that supports an alternative option for os-shell (e.g. Python).
* Added: New option "--icmp-exfil" that supports the "ICMP exfiltration" injection technique (module).
* Added: The "tempfile-based" (semiblind) technique.
* Added: The "file-based" (semiblind) technique.
* Removed: The "boolean-based" (blind) technique.
* Added: More Options.

## Version 0.1a (2014-20-12)
* The initial release {aka the Birth!}.
