# Hacktoberfest Troubleshooting Guide

This guide helps you resolve common issues encountered during Hacktoberfest 2025 participation.

## 📚 Table of Contents

- [Registration Issues](#registration-issues)
- [Repository Eligibility](#repository-eligibility)
- [Pull Request Problems](#pull-request-problems)
- [Git and GitHub Issues](#git-and-github-issues)
- [Contribution Tracking](#contribution-tracking)
- [Common Error Messages](#common-error-messages)
- [Getting Help](#getting-help)

## Registration Issues

### Issue: Can't register for Hacktoberfest
**Symptoms**: Registration button not working, error messages during signup

**Solutions**:
1. **Check Hacktoberfest Status**: Visit [hacktoberfest.com](https://hacktoberfest.com) to ensure registration is open
2. **Clear Browser Cache**: Clear cookies and cache, try incognito mode
3. **Try Different Browser**: Switch to Chrome, Firefox, or Safari
4. **Check GitHub Account**: Ensure your GitHub account is verified and active
5. **Wait and Retry**: Sometimes servers are overloaded during peak times

### Issue: "Account not eligible" error
**Solutions**:
1. **Verify Email**: Ensure your GitHub email is verified
2. **Check Account Age**: Some restrictions may apply to very new accounts
3. **Contact Support**: Reach out to Hacktoberfest support if issue persists

## Repository Eligibility

### Issue: My PRs aren't counting toward Hacktoberfest
**Symptoms**: PRs show as "ineligible" or don't appear in your Hacktoberfest dashboard

**Solutions**:
1. **Check Repository Topics**: Repository must have `hacktoberfest` topic
   ```bash
   # Check repository topics on GitHub
   # Go to repository → About section → Topics
   ```

2. **Verify PR Labels**: PR should be labeled `hacktoberfest-accepted` or merged
3. **Check PR Status**: Must be merged or approved, not just open
4. **Repository Must Be Public**: Private repositories don't count
5. **Check PR Date**: Must be submitted between October 1-31

### Issue: Repository doesn't have hacktoberfest topic
**Solutions**:
1. **Contact Maintainers**: Ask them to add the topic
2. **Find Alternative Repos**: Look for repositories that already have the topic
3. **Check Official Lists**: Use Hacktoberfest's official repository lists

## Pull Request Problems

### Issue: PR rejected or closed without merge
**Symptoms**: PR closed with "invalid" or "spam" labels

**Solutions**:
1. **Read Guidelines**: Carefully read CONTRIBUTING.md and README.md
2. **Improve Quality**: Ensure your contribution adds real value
3. **Follow Standards**: Match the project's coding style and conventions
4. **Add Tests**: Include tests for your changes when applicable
5. **Write Good Descriptions**: Explain what your PR does and why

### Issue: PR stuck in review
**Symptoms**: PR open for days/weeks without response

**Solutions**:
1. **Be Patient**: Maintainers are often volunteers with limited time
2. **Ping Politely**: Comment asking for status update after a week
3. **Check Activity**: Look at recent commits to see if project is active
4. **Find Alternatives**: Consider contributing to more active repositories

### Issue: Merge conflicts
**Symptoms**: "This branch has conflicts that must be resolved"

**Solutions**:
1. **Update Your Branch**:
   ```bash
   git fetch upstream
   git checkout your-branch
   git merge upstream/main
   ```

2. **Resolve Conflicts**:
   - Open conflicted files
   - Choose which changes to keep
   - Remove conflict markers
   - Test your changes

3. **Complete Merge**:
   ```bash
   git add resolved-files
   git commit -m "Resolve merge conflicts"
   git push origin your-branch
   ```

## Git and GitHub Issues

### Issue: "Permission denied" when pushing
**Solutions**:
1. **Check Authentication**: Ensure you're logged into GitHub
2. **Use HTTPS**: Switch from SSH to HTTPS if needed
   ```bash
   git remote set-url origin https://github.com/USERNAME/REPO.git
   ```
3. **Generate New Token**: Create a new Personal Access Token
4. **Check SSH Keys**: Verify SSH key is added to GitHub account

### Issue: "Repository not found" error
**Solutions**:
1. **Check URL**: Verify the repository URL is correct
2. **Check Permissions**: Ensure you have access to the repository
3. **Fork First**: Make sure you've forked the repository
4. **Update Remote**: Check your remote URLs
   ```bash
   git remote -v
   ```

### Issue: Can't find your fork
**Solutions**:
1. **Check GitHub Profile**: Look under "Repositories" tab
2. **Search GitHub**: Use GitHub search to find your fork
3. **Check Original Repo**: Look at the "Forks" section of the original repo

## Contribution Tracking

### Issue: Contributions not showing on GitHub profile
**Solutions**:
1. **Check Privacy Settings**: Ensure contributions are public
2. **Verify Email**: Use the same email for commits and GitHub account
3. **Wait for Sync**: GitHub can take up to 24 hours to update
4. **Check Date Range**: Contributions must be within the current year

### Issue: Hacktoberfest dashboard not updating
**Solutions**:
1. **Wait for Processing**: Updates can take 24-48 hours
2. **Check PR Status**: Ensure PRs are merged or labeled correctly
3. **Refresh Page**: Clear cache and refresh the dashboard
4. **Contact Support**: Reach out if issues persist after 48 hours

## Common Error Messages

### "This pull request is not eligible for Hacktoberfest"
**Cause**: Repository doesn't have hacktoberfest topic or PR doesn't meet requirements

**Solution**: Find repositories with `hacktoberfest` topic and ensure your PR is meaningful

### "Repository is not participating in Hacktoberfest"
**Cause**: Repository maintainer hasn't opted in

**Solution**: Look for repositories that explicitly mention Hacktoberfest participation

### "Pull request is too small"
**Cause**: Contribution is considered spam (typo fixes, whitespace changes)

**Solution**: Make substantial contributions that add real value

### "Pull request is not merged"
**Cause**: PR is still open and not merged

**Solution**: Wait for maintainer to merge or find repositories with faster review times

## Getting Help

### Official Support Channels
- **Hacktoberfest Support**: [hacktoberfest.com/support](https://hacktoberfest.com/support)
- **GitHub Support**: [support.github.com](https://support.github.com)
- **Discord Community**: Join Hacktoberfest Discord server

### Community Resources
- **GitHub Discussions**: Many repositories have discussion forums
- **Reddit**: r/hacktoberfest and r/github
- **Twitter**: Follow @hacktoberfest and #hacktoberfest hashtag
- **Stack Overflow**: Tag questions with hacktoberfest

### Best Practices for Getting Help
1. **Be Specific**: Describe exactly what you're trying to do
2. **Include Details**: Share error messages, screenshots, and steps taken
3. **Search First**: Check if your question has been asked before
4. **Be Patient**: Community members are volunteers
5. **Be Respectful**: Follow community guidelines and be polite

## Prevention Tips

### Before Contributing
1. **Read Documentation**: Always read README.md and CONTRIBUTING.md
2. **Check Activity**: Look for recent commits and issues
3. **Start Small**: Begin with documentation or small bug fixes
4. **Test Locally**: Ensure your changes work before submitting

### During Contribution
1. **Follow Guidelines**: Stick to project conventions
2. **Write Good Commits**: Use clear, descriptive commit messages
3. **Test Thoroughly**: Verify your changes don't break anything
4. **Document Changes**: Explain what your code does

### After Submission
1. **Monitor PR**: Respond to feedback promptly
2. **Be Open to Changes**: Accept suggestions and improvements
3. **Stay Engaged**: Participate in discussions and reviews
4. **Learn from Feedback**: Use maintainer feedback to improve

## Quick Reference

### Essential Commands
```bash
# Check repository topics
# Visit: https://github.com/OWNER/REPO

# Check PR status
# Visit: https://github.com/OWNER/REPO/pulls

# Update fork
git fetch upstream
git merge upstream/main
git push origin main

# Check contribution status
# Visit: https://hacktoberfest.com/profile
```

### Useful Links
- [Hacktoberfest Official Site](https://hacktoberfest.com)
- [GitHub Topics Search](https://github.com/topics/hacktoberfest)
- [First Contributions Guide](https://firstcontributions.github.io)
- [GitHub Learning Lab](https://lab.github.com)

---

**Remember**: Hacktoberfest is about learning and contributing to open source. Don't get discouraged by setbacks - they're part of the learning process! 🚀
