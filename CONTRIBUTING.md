# Contributing to Titanic Survival Prediction Project

Thank you for your interest in contributing! This document provides guidelines and instructions for contributing to this project.

---

## 🎯 How to Contribute

### 1. Report Issues
If you find a bug or have a suggestion:
- Create an Issue with clear description
- Include steps to reproduce (if it's a bug)
- Attach relevant code snippets or error messages
- Suggest a solution if you have one

### 2. Improve Documentation
- Fix typos or unclear explanations
- Add examples to README
- Improve code comments
- Add diagrams or visualizations

### 3. Add New Features
- Implement new algorithms
- Create additional analysis
- Add new visualizations
- Improve data preprocessing

### 4. Code Improvements
- Refactor existing code
- Optimize performance
- Add error handling
- Improve code quality

---

## 📋 Contribution Workflow

### Step 1: Fork the Repository
```bash
# Click "Fork" on GitHub (if hosted there)
```

### Step 2: Clone Your Fork
```bash
git clone https://github.com/YOUR-USERNAME/ML-Titanic-Dataset.git
cd ML-Titanic-Dataset
```

### Step 3: Create a Feature Branch
```bash
git checkout -b feature/your-feature-name
# OR for bug fixes:
git checkout -b bugfix/issue-description
```

### Step 4: Make Your Changes
- Edit files as needed
- Follow the coding standards below
- Test your changes thoroughly

### Step 5: Commit Your Changes
```bash
git add .
git commit -m "feat: add your feature description"
# OR
git commit -m "fix: resolve issue with model accuracy"
# OR
git commit -m "docs: update README with new examples"
```

### Step 6: Push to Your Fork
```bash
git push origin feature/your-feature-name
```

### Step 7: Create a Pull Request
- Go to GitHub and create a Pull Request
- Use clear title and description
- Link related issues
- Wait for review

---

## 📐 Coding Standards

### Python Code Style
- Follow **PEP 8** conventions
- Use 4 spaces for indentation (not tabs)
- Maximum line length: 100 characters
- Use descriptive variable names

### Example:
```python
# ✅ GOOD
def calculate_model_accuracy(predictions, actual_labels):
    """
    Calculate accuracy of model predictions.
    
    Args:
        predictions: Array of predicted labels
        actual_labels: Array of ground truth labels
        
    Returns:
        float: Accuracy score between 0 and 1
    """
    correct = sum(predictions == actual_labels)
    accuracy = correct / len(actual_labels)
    return accuracy

# ❌ BAD
def calc_acc(pred, act):
    return sum(pred == act) / len(act)
```

### Notebook Standards
- Clear section headers with markdown
- Comments explaining complex code
- Output visualization after analysis
- No hardcoded paths (use relative paths)
- Random seeds set for reproducibility

```python
# ✅ GOOD
# Set random seeds for reproducibility
np.random.seed(42)
sklearn.random_state = 42

# Load dataset
df = pd.read_csv('titanic.csv')

# ❌ BAD
df = pd.read_csv('C:/Users/Username/Data/titanic.csv')
```

---

## 🧪 Testing Guidelines

Before submitting a Pull Request:

1. **Run All Notebooks**
   ```bash
   jupyter nbconvert --to notebook --execute titanic_*.ipynb
   ```

2. **Check for Errors**
   - All cells should execute without errors
   - Output should be reasonable

3. **Verify Results**
   - Model accuracy should be in expected range
   - No data leakage
   - Proper train-test split

4. **Visual Inspection**
   - Plots are generated correctly
   - Data looks reasonable
   - No obvious bugs in visualizations

---

## 📝 Commit Message Guidelines

Use clear, descriptive commit messages:

```
# Format: type: description

# Types:
# feat:     New feature
# fix:      Bug fix
# docs:     Documentation update
# style:    Code style changes
# refactor: Code refactoring
# perf:     Performance improvement
# test:     Test additions

# Examples:
git commit -m "feat: add gradient boosting notebook"
git commit -m "fix: correct data preprocessing in logistic regression"
git commit -m "docs: improve README with usage examples"
git commit -m "refactor: optimize data loading function"
git commit -m "perf: improve model training speed by 20%"
```

---

## 🔍 Code Review Process

### What We Look For:
- ✅ Code follows style guidelines
- ✅ Changes are well-documented
- ✅ Notebooks run without errors
- ✅ Results are reasonable
- ✅ No major performance degradation
- ✅ Commit messages are clear
- ✅ Changes align with project goals

### Feedback
- Be respectful and constructive
- Explain reasoning for suggestions
- Ask questions if unclear
- Acknowledge good contributions

---

## 🎓 Project Structure Guidelines

### Adding New Notebooks
1. Use consistent naming: `titanic_[algorithm_name].ipynb`
2. Follow the standard notebook structure:
   - Import Libraries
   - Load Dataset
   - Data Exploration
   - Preprocessing
   - Model Training
   - Evaluation
   - Visualization

### Adding New Documentation
1. Update README.md if adding major features
2. Update ANALYSIS.md with new findings
3. Keep documentation in sync with code

### Adding New Models
1. Create notebook following template
2. Compare with existing models
3. Add to performance comparison table
4. Include hyperparameter tuning section

---

## 📚 Documentation Requirements

### For New Features:
- [ ] Code comments explaining logic
- [ ] Docstrings for functions
- [ ] Section headers in notebooks
- [ ] Markdown cells explaining steps
- [ ] Update README.md with overview
- [ ] Update ANALYSIS.md with comparison

### Example:
```python
def preprocess_data(df):
    """
    Preprocess Titanic dataset for modeling.
    
    Steps:
    1. Drop non-predictive columns
    2. Handle missing values
    3. Encode categorical variables
    4. Scale numerical features
    
    Args:
        df (pd.DataFrame): Raw dataset
        
    Returns:
        pd.DataFrame: Processed dataset ready for modeling
    """
    # Implementation
    return processed_df
```

---

## ⚠️ What NOT to Do

- ❌ Don't hardcode file paths
- ❌ Don't commit large data files
- ❌ Don't remove existing tests
- ❌ Don't change random seeds (breaks reproducibility)
- ❌ Don't use unclear variable names
- ❌ Don't add unrelated changes to one PR
- ❌ Don't force push to main branch

---

## 🚀 Getting Help

- **Questions?** Open an Issue with "question:" prefix
- **Unclear requirements?** Comment on the Issue
- **Need guidance?** Ask for help in discussions
- **Found a bug?** Create a detailed bug report

---

## 📜 Code of Conduct

- Be respectful and inclusive
- Welcome diverse perspectives
- Focus on constructive feedback
- No harassment or discrimination
- Respect confidentiality
- Report violations appropriately

---

## 🎁 Contributor Recognition

We appreciate all contributions! Contributors will be:
- Acknowledged in README.md
- Featured in release notes
- Recognized in commit history

---

## 📋 Contribution Checklist

Before submitting a Pull Request, ensure:

- [ ] Code follows PEP 8 style guide
- [ ] All notebooks run without errors
- [ ] No hardcoded paths or credentials
- [ ] Changes are well-documented
- [ ] Commit messages are clear
- [ ] No large files committed
- [ ] Tests pass (if applicable)
- [ ] Documentation is updated
- [ ] Feature is aligned with project goals

---

## 🙏 Thank You!

Your contributions help make this project better for everyone. We appreciate your time and effort!

---

**Last Updated**: January 2026  
**Version**: 1.0
