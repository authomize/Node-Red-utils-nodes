# Node-Red-utils-nodes

This package provides two custom nodes for Node-RED.

## Nodes

### any_split

Splits the input message based on any specified property, not limited to `msg.payload`.

### custom_diff

Compares two lists and returns the differences between them. It takes two input lists:

- `listA`: List of current state (Users we would like to have on the destination group we create).
- `listB`: List of destination group.

This node returns two lists as outputs:

- `create`: Contains all users that are in `listA` but not in `listB`, indicating that they need to be created on the destination platform.
- `remove`: Contains all users that are in `listB` but not in `listA`, indicating that they need to be deleted from the destination platform.

Both `create` and `remove` lists will be available as properties (`msg.create` and `msg.remove`) in the node's output message.

## Usage

1. Install the Node-Red-utils-nodes package using npm: npm i  node-red-utils-nodes

2. In your Node-RED flow, you will find the `any_split` and `custom_diff` nodes under the "Authomize utils" category in the Node-RED palette.

3. Drag and drop the desired node into your flow and configure its properties as required.

4. Connect the input and output nodes to complete your flow.

## Contributing

Contributions, bug reports, and feature requests are welcome!

## License

This project is licensed under the [MIT License](LICENSE).
