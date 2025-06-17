# Proxy contract

### **Purpose**

* The DSProxy contract allows users to execute code on their behalf using a persistent proxy address.
* It simplifies complex multi-step operations by enabling atomic execution within the context of the proxy’s identity.
* Ownership of the proxy is flexible and can be transferred, supporting dynamic models like multisignature wallets.

### Key Methods

* `execute(bytes memory _code, bytes memory _data)`
  * If \_code corresponds to a cached contract, it is executed directly; otherwise, the contract is deployed and cached before execution.
  * \_data specifies the calldata to be sent to the contract.
  * Emits an Execute event upon successful execution.
* `execute(address _target, bytes memory _data)`
  * Directly executes a specified contract (\_target) with provided calldata (\_data).
  * Requires the caller to have the necessary auth permissions.
