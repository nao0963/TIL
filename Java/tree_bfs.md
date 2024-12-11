# tree_bfs

## What I Learned
- how to make traversal by using bfs
- Understanding of Queue from error I made
- If there's **null** value in queue, queue is **not empty**

## error code
    public void bfs(MyTreeNode root) {
        Queue<MyTreeNode> queue = new LinkedList<MyTreeNode>();
        queue.add(root);
        while(!queue.isEmpty()) {
            MyTreeNode node = queue.poll();
            System.out.print(node.data+" ");

            queue.add(node.leftChild);
            queue.add(node.rightChild);

        }
    }



## fixed code
    public void bfs(MyTreeNode root) {
        Queue<MyTreeNode> queue = new LinkedList<MyTreeNode>();
        queue.add(root);
        while (!queue.isEmpty()) {
            MyTreeNode node = queue.poll();
            System.out.print(node.data + " ");
            if (node.leftChild != null) {
                queue.add(node.leftChild);
            }
            if (node.rightChild != null) {
                queue.add(node.rightChild);
            }

        }
    }

    
