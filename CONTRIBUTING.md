# Contributing to BLE-Sensor

Thank you for your interest in contributing to the BLE-Sensor project! We welcome contributions from the community.

## How to Contribute

### Reporting Issues
- Use the GitHub issue tracker
- Describe the issue clearly
- Include steps to reproduce
- Provide relevant hardware/software versions

### Suggesting Enhancements
- Open an issue with the "enhancement" label
- Describe the proposed feature
- Explain the use case and benefits

### Pull Requests
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/your-feature`)
3. Make your changes
4. Test your changes thoroughly
5. Commit with clear messages (`git commit -m 'Add feature'`)
6. Push to your fork (`git push origin feature/your-feature`)
7. Open a Pull Request

## Development Guidelines

### Hardware Design
- Follow the existing design patterns
- Document all changes
- Update schematics and PCB layout
- Update BOM if components change
- Follow RF design best practices for BLE

### Firmware Development
- Follow the existing code style
- Comment your code appropriately
- Test on hardware if possible
- Update documentation
- Keep commits focused and atomic

### Documentation
- Use clear, concise language
- Include examples where helpful
- Update relevant README files
- Add images/diagrams if needed

## Code Style

### C/C++ (Firmware)
- Use K&R or Allman brace style (be consistent)
- Indent with spaces (2 or 4 spaces)
- Comment complex logic
- Use meaningful variable names
- Follow STM32 HAL conventions

### Markdown (Documentation)
- Use proper heading hierarchy
- Include code blocks with syntax highlighting
- Keep lines under 100 characters when possible

## Testing

### Hardware Testing
- Verify electrical specifications
- Test RF performance
- Check power consumption
- Validate sensor accuracy

### Firmware Testing
- Test on actual hardware
- Verify BLE functionality
- Check power modes
- Validate sensor readings

## Commit Message Guidelines

- Use present tense ("Add feature" not "Added feature")
- Use imperative mood ("Move cursor to..." not "Moves cursor to...")
- Limit first line to 72 characters
- Reference issues and pull requests

Example:
```
Add temperature sensor driver

- Implement I2C communication
- Add sensor initialization
- Include calibration routine

Fixes #123
```

## License

By contributing, you agree that your contributions will be licensed under the MIT License.

## Questions?

Feel free to open an issue for questions or discussion.
