# Texture01

#旋转矩阵翻转图形,不翻转纹理

#让图形顶点坐标旋转180°. 而纹理保持原状.

GLuint rotate = glGetUniformLocation(self.myPrograme, "rotateMatrix");
    float radians = 180 * 3.14159f / 180.0f;
    float s = sin(radians);
    float c = cos(radians);
    
  
    GLfloat zRotation[16] = {
        -c, s, 0, 0,
        -s, c, 0, 0,
        0, 0, 1.0, 0,
        0.0, 0, 0, 1.0
    };
    
   glUniformMatrix4fv(rotate, 1, GL_FALSE, (GLfloat *)&zRotation[0]);
