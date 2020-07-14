# cfn-util

Cloudformation utility scripts, desiged for use when debugging/developing Cloudformation in a sandbox account.

* `cfn-create` creates a stack. You can specify parameters as `-P Name=Value` (can be used multiple times). WARNING: the stack is deleted first if it exists.
* `cfn-update` updates a stack. This works just like `cfn-create` but does does not attempt a delete first, and uses the `update-stack` command underneath.
* `cfn-show` shows you a stack's current resource status and any failure events since last create/update. Hook it up to `watch` or [ww](hhtps://github.com/jtyers/ww) and you have an easy way to monitor stack status from your terminal without having to resort to constantly clicking 'Refresh' in the AWS Console
