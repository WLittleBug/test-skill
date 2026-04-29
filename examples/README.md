# Test Skill Examples

This directory contains example usage patterns for the test-skill.

## Basic Usage

```python
# Simple repository creation
mcp_github_create_repository(
    name="example-repo",
    description="An example repository",
    private=False
)

# File operations
mcp_github_create_or_update_file(
    owner="WLittleBug",
    repo="test-skill",
    path="examples/hello.py",
    content="print('Hello from Hermes Agent!')",
    message="Add hello.py example",
    branch="main"
)
```

## Advanced Usage

```python
# Multiple file operations
mcp_github_push_files(
    owner="WLittleBug",
    repo="test-skill",
    branch="main",
    message="Add multiple example files",
    files=[
        {
            "path": "examples/config.yaml",
            "content": "config:\n  enabled: true\n  timeout: 30"
        },
        {
            "path": "examples/README.md", 
            "content": "# Examples\n\nVarious usage examples for the test skill"
        }
    ]
)
```

## Error Handling

```python
try:
    result = mcp_github_get_file_contents(
        owner="WLittleBug",
        repo="test-skill",
        path="nonexistent.txt"
    )
except Exception as e:
    print(f"Error: {e}")
    # Handle error appropriately
```