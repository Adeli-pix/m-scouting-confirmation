M SCOUTING EMAIL CONFIRMATION PAGE

Files:
- index.html: confirmation page
- m_scouting_eyes_banner.png: original artwork copied unchanged from your supplied ZIP

HOW TO USE
1. Upload both index.html and m_scouting_eyes_banner.png to the same folder in your GitHub Pages repository.
2. Enable GitHub Pages for that repository.
3. In Supabase > Authentication > URL Configuration, set Site URL to your published GitHub Pages URL and add that URL to Redirect URLs.
4. Your desktop app's sign-up request should set emailRedirectTo to the published page URL.
5. For a reliable click-to-confirm experience, set the Supabase confirmation email template link to:
   {{ .SiteURL }}/?token_hash={{ .TokenHash }}&type=signup
   Make sure the redirect destination is allowed in Supabase Redirect URLs.
6. Test with a fresh signup and a new confirmation email.

SECURITY
- The page contains only a publishable client key, never a service_role key.
- The page reports success only when Supabase returns a confirmed user.
- Real email confirmation has not been tested from this generated package.

ANIMATION NOTE
The original supplied banner is preserved unchanged. This package adds the confirmation interface and loading animation. It does NOT yet contain isolated eyelid/tomoe animation layers; rotating the whole banner would distort the artwork, so eye animation needs carefully masked layers aligned to the original image.
