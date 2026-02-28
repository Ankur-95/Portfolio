

# Integrate EmailJS for Contact Form

EmailJS is a client-side email service -- its public key is designed to be used in frontend code, so it's safe to store directly in the codebase.

## What will change

### Install `@emailjs/browser` package
Add the EmailJS SDK dependency.

### Update `src/components/sections/Contact.tsx`
- Import `emailjs` from `@emailjs/browser`
- Replace the current Formspree/mailto logic in `handleSubmit` with `emailjs.sendForm()` using your credentials:
  - Service ID: `service_5zvm1pi`
  - Template ID: `template_cnu08xj`
  - Public Key: `euVOrR_3cpj8GUt4m`
- Add loading state and error handling with a toast notification
- On success: show the "Message Sent!" confirmation
- On failure: show an error toast so the user knows something went wrong

### EmailJS Template Requirements
Your EmailJS template must use these template variables (matching the form field `name` attributes):
- `{{name}}` -- sender's name
- `{{email}}` -- sender's email
- `{{message}}` -- the message content

Make sure your template on the EmailJS dashboard uses these exact variable names, or the fields won't populate in the email you receive.

## Technical Details

The `handleSubmit` function will be rewritten to:

```typescript
const handleSubmit = async (e: React.FormEvent<HTMLFormElement>) => {
  e.preventDefault();
  setLoading(true);
  try {
    await emailjs.sendForm(
      'service_5zvm1pi',
      'template_cnu08xj',
      e.currentTarget,
      'euVOrR_3cpj8GUt4m'
    );
    setSubmitted(true);
    toast({ title: "Message sent!", description: "I'll get back to you soon." });
  } catch (error) {
    toast({ title: "Failed to send", description: "Please try again.", variant: "destructive" });
  } finally {
    setLoading(false);
  }
};
```

## Files modified
| File | Change |
|------|--------|
| `package.json` | Add `@emailjs/browser` dependency |
| `src/components/sections/Contact.tsx` | Replace Formspree/mailto with EmailJS integration, add loading/error states |

