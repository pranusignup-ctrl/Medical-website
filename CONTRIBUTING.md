# Contributing to Dr. J Pranay Kumar's Medical Website

Thank you for your interest in contributing to this premium medical website project! We welcome contributions that help improve the healthcare experience for patients.

## Code of Conduct

- Be respectful and professional
- Focus on patient privacy and data security
- Maintain healthcare compliance standards
- Follow accessibility guidelines

## How to Contribute

### 1. Fork and Clone
```bash
git clone https://github.com/pranusignup-ctrl/medical-website.git
cd medical-website
```

### 2. Create a Feature Branch
```bash
git checkout -b feature/your-feature-name
```

### 3. Make Your Changes

Follow these guidelines:
- **HTML**: Keep semantic markup clean and accessible
- **CSS**: Maintain responsive design principles
- **JavaScript**: Use vanilla JS, avoid unnecessary dependencies

### 4. Test Your Changes

- Test on desktop, tablet, and mobile
- Test light and dark modes
- Verify form validation
- Check accessibility

### 5. Commit Your Changes

```bash
git commit -m "Add: descriptive message of your changes"
```

Use these prefixes:
- `Add:` for new features
- `Fix:` for bug fixes
- `Improve:` for improvements
- `Refactor:` for code refactoring
- `Docs:` for documentation updates

### 6. Push and Create Pull Request

```bash
git push origin feature/your-feature-name
```

Then create a Pull Request on GitHub with a clear description.

## Development Guidelines

### HTML Structure
- Use semantic HTML5 elements
- Include proper ARIA labels for accessibility
- Maintain clean indentation

### CSS Styling
- Follow the existing color scheme
- Maintain responsive breakpoints
- Use CSS variables for colors
- Add animations smoothly

### JavaScript
- Use modern ES6+ syntax
- Write clear, commented code
- Avoid global variables
- Test form validation thoroughly

## Reporting Issues

When reporting issues:
1. Check if the issue already exists
2. Provide a clear description
3. Include steps to reproduce
4. Specify browser and device
5. Include screenshots if relevant

## Feature Requests

Feature requests should include:
- Clear use case
- Benefits to patients
- Implementation suggestions
- Any security considerations

## Security Considerations

For any security-related changes:
- Never commit sensitive data
- Follow HIPAA guidelines
- Implement proper validation
- Use secure communication protocols
- Document security measures

## Naming Conventions

### Variables
```javascript
// Good
const appointmentDate = "2024-07-01";
let patientFormData = {};

// Avoid
const appDate = "2024-07-01";
let pfd = {};
```

### Functions
```javascript
// Good
function validatePhoneNumber(phone) { }
function sendAppointmentConfirmation(data) { }

// Avoid
function validate(p) { }
function send(d) { }
```

### CSS Classes
```css
/* Good */
.appointment-form
.patient-info-section
.emergency-button

/* Avoid */
.ap-form
.p-info
.emg-btn
```

## Documentation

When adding new features, update:
- `README.md` with feature description
- Comments in code
- This CONTRIBUTING.md if needed

## Testing Checklist

Before submitting a PR, verify:
- [ ] All forms work correctly
- [ ] Responsive design at all breakpoints
- [ ] Dark mode functions properly
- [ ] Accessibility standards met
- [ ] No console errors
- [ ] No broken links
- [ ] Email/SMS placeholders work
- [ ] Animations are smooth
- [ ] Mobile navigation works
- [ ] Patient data is secure

## Performance Guidelines

- Minimize CSS/JS file sizes
- Optimize images
- Lazy load where appropriate
- Avoid render-blocking resources
- Test page load times

## Accessibility Standards

Follow WCAG 2.1 guidelines:
- Proper heading hierarchy
- Alt text for images
- Color contrast ratios
- Keyboard navigation
- Screen reader compatibility

## Need Help?

- Check existing issues and discussions
- Review the README.md
- Look at similar implementations
- Contact: hello@drpranay.com

## Commit Message Format

```
[Type]: Brief description of changes

More detailed explanation if needed.
Related issue: #123
```

### Types
- `feat:` new feature
- `fix:` bug fix
- `refactor:` code refactoring
- `style:` formatting changes
- `docs:` documentation updates
- `perf:` performance improvements
- `security:` security updates

## Pull Request Template

```markdown
## Description
Brief description of changes

## Type of Change
- [ ] New feature
- [ ] Bug fix
- [ ] Documentation update
- [ ] Security improvement

## Testing
Describe testing performed

## Checklist
- [ ] Code follows style guidelines
- [ ] Responsive design verified
- [ ] Accessibility checked
- [ ] Documentation updated
- [ ] No console errors

## Related Issues
Closes #(issue number)
```

## Code Review Process

1. Maintainer reviews code
2. Feedback provided if needed
3. Changes requested or approved
4. Merge to main branch

## Recognition

Contributors will be recognized in:
- README.md Contributors section
- GitHub contributions graph
- Project credits

## License

By contributing, you agree that your contributions will be licensed under the MIT License.

## Questions?

For questions about contributing:
- Create an issue with "question" label
- Email: hello@drpranay.com
- Contact through the website

---

Thank you for making Dr. Pranay Kumar's medical website better! 🏥❤️
